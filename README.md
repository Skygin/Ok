

package A;

public class A {

  public static void main(String[] args) {
    System.out.println("Hello, World!");
  }
}



import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;
import java.io.FileInputStream;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (FileInputStream fis = new FileInputStream("path/to/your/excel/file.xlsx")) {
            Workbook workbook = new XSSFWorkbook(fis);
            Sheet sheet = workbook.getSheetAt(0);
            Row row = sheet.getRow(0);
            Cell cell = row.getCell(0);
            System.out.println(cell.getStringCellValue());
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}







