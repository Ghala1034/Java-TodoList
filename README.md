# Java-TodoList
import java.util.ArrayList;
import java.util.Scanner;

public class TodoList {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        ArrayList<String> tasks = new ArrayList<>();

        int choice = 0;

        while (choice != 3) {

            System.out.println("1. Add Task");
            System.out.println("2. Show Tasks");
            System.out.println("3. Exit");

            System.out.print("Choose: ");
            choice = input.nextInt();
            input.nextLine();

            if (choice == 1) {
                System.out.print("Enter task: ");
                String task = input.nextLine();
                tasks.add(task);
            }

            else if (choice == 2) {
                for (int i = 0; i < tasks.size(); i++) {
                    System.out.println((i + 1) + ". " + tasks.get(i));
                }
            }
        }

        System.out.println("Goodbye!");
    }
}



وش وظيفة ArrayList<String> tasks ؟
	2.	ليش استخدمنا while ؟
	3.	وش تسوي tasks.add(task) ؟
	4.	داخل الـ for وش معنى tasks.get(i) ؟
	5.	كيف ممكن تضيفين خيار رقم 4 لحذف مهمة؟


برنامج بسيط مكتوب بلغة Java لإدارة المهام اليومية (Todo List) عبر الشاشة السوداء (Console)، يسمح للمستخدم بإضافة المهام، استعراضها، وحذفها.
🔍 تحليل وفهم الكود (Code Analysis)
 إدارة البيانات باستخدام ⁠ArrayList⁠:
استخدمنا ⁠ArrayList<String>⁠ كقائمة ديناميكية مرنة لتخزين نصوص المهام؛ لأن حجمها يتغير تلقائياً مع كل عملية إضافة أو حذف، عكس المصفوفات العادية ثنائية الحجم.
 التحكم بالبرنامج باستخدام ⁠while loop⁠:
تم استخدام حلقة التكرار ⁠while (choice != 4)⁠ لضمان استمرار ظهور قائمة الخيارات للمستخدم بشكل متكرر، ولا يتوقف البرنامج عن العمل إلا إذا قام المستخدم باختيار رقم الخروج (الرقم 4).
 إضافة المهام باستخدام ⁠.add()⁠:
دالة ⁠tasks.add(task)⁠ مسؤولة عن أخذ النص الذي كتبه المستخدم وحفظه وتخزينه داخل القائمة (المصفوفة)، وليست دالة طباعة.
 استعراض المهام باستخدام ⁠for loop⁠ ودالة ⁠.get()⁠:
قمنا بعمل حلقة تكرار ⁠for⁠ للمرور على جميع المهام المخزنة، واستخدمنا الدالة ⁠tasks.get(i)⁠ لجلب واستدعاء المهمة الموجودة في الموقع رقم (i) لكي يتم طباعتها للمستخدم بشكل مرتب (1, 2, 3...).
 حذف المهام باستخدام ⁠.remove()⁠:
أضفنا دالة الحذف ⁠tasks.remove(taskNumber - 1)⁠ لتسمح للمستخدم بحذف مهمة معينة بناءً على رقمها، مع طرح رقم 1 لأن ترقيم القوائم في الجافا (Index) يبدأ دائماً من الصفر.
