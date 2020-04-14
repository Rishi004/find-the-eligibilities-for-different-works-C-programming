// find-the-eligibilities-for-different-works-C-programming
// loop only
// this program is going to dispaly eligibility for different works
#include<stdio.h>

int main(void)
{
    char name[50];
    int applicants, age, studies, work_experience, assistant_managerscount=0, computer_operatorscount=0, labourerscount=0, score=0;
    
    for(applicants=1; applicants<=5; applicants++)
    {
        printf("Enter your First name: ");
        scanf("%s", name);
        
        printf("Enter your age: ");
        scanf("%d", &age);
        if(age>=25)
        {
           printf("Your study status(1 for Degree / 2 for A/L / 3 for O/L): ");
           scanf("%d", &studies);
           if(studies==1)
                score+=5;
           else if(studies==2)
                    score+=3;
                else if(studies==3)
                        score+=2;
                     else
                        score+=0;
            
            printf("Do you have work experience(1 for Yes / 2 for No): ");
            scanf("%d", &work_experience);
            if(work_experience==1)
                score+=3;
            else
                score+=0;

	    printf("\n");
        }
        else
        printf("Sorry you are not eligible for this factory\n\n");
        
        if(score>=8)
            assistant_managerscount++;
        if(score>=6 && score<8)
            computer_operatorscount++;
        if(score>=2 && score<6)
            labourerscount++;

	score=0;
    }
    
    printf("Total selected Assistant managers: %d\n", assistant_managerscount);
    printf("Total selected Computer operators: %d\n", computer_operatorscount);
    printf("Total selected Labourers: %d\n\n", labourerscount);
    
    printf("Total Advance salary for Assistant managers: Rs. %.2f\n", assistant_managerscount*60000.00);
    printf("Total Advance salary for Computer operators: Rs. %.2f\n", computer_operatorscount*40000.00);
    printf("Total Advance salary for Labourers: Rs. %.2f\n", labourerscount*35000.00);
    
    return 0;
}
