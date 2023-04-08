# 1.
const fs = require('fs'); // require the built-in Node.js file system module

fs.readdir('.', (err, files) => { // read the current directory asynchronously
  if (err) { // check for errors
    console.error(err); // log the error to the console
    return; // return from the function to prevent further execution
  }

  files.forEach(file => { // loop through each file in the directory
    console.log(file); // log the name of the file to the console
  });
});



2.
Student.find({ status: 'student' })
        .populate('student')
        .exec(function (err, students) {
            if (err) {
                return res.status(400).send({
                    message: errorHandler.getErrorMessage(err)
                });
            }
           _.forEach(students, function (student) {
    console.log('Student:', student);
    console.log('Time entries:', student.worksnapsTimeEntries);
});
            res.json(students);
        });

// Loop through each student in the result set and log information to the console
_.forEach(students, function (student) {
    console.log('Student:', student); // log the student object
    console.log('Time entries:', student.worksnapsTimeEntries); // log the student's work times
});

res.json(students); // return the result set as JSON


/* _.forEach(students, function (student) {
    student = student.toObject(); // Convert Mongoose object to plain JavaScript object
    student.worksnapsTimeEntries = student.worksnapsTimeEntries || []; // Ensure the array exists
    res.json(student);
});
*/

4.function isPrime(number) {
  // First, we check if the number is less than 2. If it is, we know it's not prime, so we return false.
  if (number < 2) {
    return false;
  }

  // We loop from 2 to the square root of the number.
  for (let i = 2; i <= Math.sqrt(number); i++) {
    // If the number is divisible by i, it's not prime, so we return false.
    if (number % i === 0) {
      return false;
    }
  }

  // If we haven't found any factors, the number is prime, so we return true.
  return true;
}
5.
public static void main(String[] args)
{
    int n = 6; // The height of the pyramid
    System.out.print("Enter Symbol : ");
    char c = sc.next().charAt(0); // The symbol to use in the pyramid

    int i = n;
    int j;	

    do 
    {
        // If we're on the first or last row of the pyramid...
        if (i == 1 || i == n)
        {
            j = 1;
            // Print out the given symbol for the entire row
            do
            {
                System.out.print(c);
            } while (++j <= i);
        }
        else
        {
            j = 1;
            // Print out the given symbol for the first and last character of the row,
            // and spaces for everything in between
            do
            {
                if (j == 1 || j == i)
                    System.out.print(c);
                else
                    System.out.print(" ");
            } while (++j <= i);
        }
        // Move to the next row
        System.out.println();
    } while (--i > 0);           
}
