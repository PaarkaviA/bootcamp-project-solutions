# bootcamp-project-solutions


List of Capstone Projects
NUMBERS:

  Find PI to the Nth Digit:
  from math import e
def given_num(n):
   
    return '%.*f' % (n, e)

if __name__ == '__main__':
    # there is no do while loop in python, so we need to improvise
    correct_input = False
    while not correct_input:
        # ask until you get correct input
        print('Precision must be between 1 and 100')
        no_of_dec = int(input('Number of decimal places: '))
        if 100 >= no_of_dec > 0:
            correct_input = True
    print(given_num(no_of_dec))
    
    
    prog 2:
    givenum = input("num : ")
    for n in givenum:
    print("e")
    
    output:
    num = 10 
    e 
    e 
    (e is imported then output will be
    the same as the above prog)
FIBONACCI SERIES:
TO PRINT SEQUENCE:
no_of_terms = int(input("enter to num to print the fibo seq upto : "))
n1,n2 = 0,1
count = 0
if no_of_terms <= 0:
    print('enter positive interger')
elif no_of_terms == 1:
    print('the fibo sequence upto ',no_of_terms,'is')
    print (n1)
else:
    while count < no_of_terms:
        print(n1)
        nth = n1+n2
        n1 = n2
        n2 = nth
        count += 1
        
 TO GET A FIB NUM IN A PARTICULAR PLACE:
 def fibo(n):

    if n <= 0:
        print("enter a positive integer")
    elif n == 0:
        return(0)
    elif n == 1 or n == 2:
        return(1)
    else :
        return fibo(n-1) + fibo(n-2)

print(fibo(10))
   
   
solution programdef fib(N):
    if N == 1:
        return [1, 0]
    else:
        terms = fib(N - 1)
        terms = [terms[0] + terms[1], terms[0]]
        return terms


def validate_positive_integer():
    while True:
        s = input("Which term in the Fibonacci sequence you want to see? ")
        try:
            N = int(s)
            if N >= 500:
                print ("Enter a number smaller than 500.")
            elif N > 0:
                return N
            else:
                print ("Enter a positive integer.")
        except ValueError:
            print ("Enter a positive integer.")


def main():
    N = validate_positive_integer()
    print (fib(N)[1])


if __name__ == "__main__":
    main()
