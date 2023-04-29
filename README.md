1)

public static double meanOfMoreThan150(int[] array) {
    int sum = 0;
    int count = 0;

    for (int i = 0; i < array.length; i++) {
        sum += array[i];
        count++;

        if (count > 150) {
            return (double) sum / count;
        }
    }

    // If there are less than 150 elements in the array, return 0.
    return 0;
}

2)

public static double averageOfOddNumbers(int[] array) {
    int sum = 0;
    int count = 0;

    for (int i = 0; i < array.length; i++) {
        if (array[i] % 2 != 0) {  // check if the number is odd
            sum += array[i];
            count++;
        }
    }

    if (count > 0) {  // check if there are any odd numbers
        return (double) sum / count;
    } else {
        return 0;  // if there are no odd numbers, return 0
    }
}


3)

public class Department {
    private String name;
    private String location;
    private int numberOfEmployees;
    private boolean isOpen;

    public Department(String name, String location, int numberOfEmployees, boolean isOpen) {
        this.name = name;
        this.location = location;
        this.numberOfEmployees = numberOfEmployees;
        this.isOpen = isOpen;
    }

    // Getters and setters for the fields

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getLocation() {
        return location;
    }

    public void setLocation(String location) {
        this.location = location;
    }

    public int getNumberOfEmployees() {
        return numberOfEmployees;
    }

    public void setNumberOfEmployees(int numberOfEmployees) {
        this.numberOfEmployees = numberOfEmployees;
    }

    public boolean isOpen() {
        return isOpen;
    }

    public void setOpen(boolean isOpen) {
        this.isOpen = isOpen;
    }

    // toString() method to return a string representation of the department object

    @Override
    public String toString() {
        return "Department{" +
                "name='" + name + '\'' +
                ", location='" + location + '\'' +
                ", numberOfEmployees=" + numberOfEmployees +
                ", isOpen=" + isOpen +
                '}';
    }

    // equals() method to check if two department objects are equal

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;

        Department that = (Department) obj;

        if (numberOfEmployees != that.numberOfEmployees) return false;
        if (isOpen != that.isOpen) return false;
        if (name != null ? !name.equals(that.name) : that.name != null) return false;
        return location != null ? location.equals(that.location) : that.location == null;
    }

}

4) 

import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class XmlWriter {
    public static void main(String[] args) {
        // create the xml string
        String xmlString = "<departments>\n" +
                "    <department>\n" +
                "        <name>HR</name>\n" +
                "        <email>hr@oracle.com</email>\n" +
                "    </department>\n" +
                "    <department>\n" +
                "        <name>IT</name>\n" +
                "        <email>it@java.com</email>\n" +
                "    </department>\n" +
                "</departments>";

        // create a file object to write the xml string to
        File xmlFile = new File("departments.xml");

        try {
            // create a file writer to write the xml string to the file
            FileWriter fileWriter = new FileWriter(xmlFile);

            // write the xml string to the file
            fileWriter.write(xmlString);

            // close the file writer
            fileWriter.close();

            System.out.println("XML file has been written to " + xmlFile.getAbsolutePath());
        } catch (IOException e) {
            System.out.println("An error occurred while writing to the file.");
            e.printStackTrace();
        }
    }
}
