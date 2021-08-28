---
description: L’exemple suivant associe une fonction d’appel de procédure asynchrone (APC), également appelée routine de saisie semi-automatique, avec un minuteur qui peut être attendu lorsque la minuterie est définie.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Utilisation de minuteries Waitables avec un appel de procédure asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62436011a3da0ac17525a0ce977e7bcd25382c5c267b62b9c972381e0f28562d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661149"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Utilisation de minuteries Waitables avec un appel de procédure asynchrone

L’exemple suivant associe une fonction d' [appel de procédure asynchrone](asynchronous-procedure-calls.md) (APC), également appelée routine de saisie semi-automatique, avec un [minuteur](waitable-timer-objects.md) qui peut être attendu lorsque la minuterie est définie. L’adresse de la routine de saisie semi-automatique est le quatrième paramètre de la fonction [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) . Le cinquième paramètre est un pointeur void que vous pouvez utiliser pour passer des arguments à la routine d’achèvement.

La routine de saisie semi-automatique sera exécutée par le même thread que celui qui a appelé [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Ce thread doit être dans un état d’alerte pour exécuter la routine de saisie semi-automatique. Pour ce faire, il appelle la fonction [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , qui est une fonction d’alerte.

Chaque thread a une file d’attente APC. S’il y a une entrée dans la file d’attente APC du thread au moment de l’appel de l’une des fonctions d’alerte, le thread n’est pas mis en veille. Au lieu de cela, l’entrée est supprimée de la file d’attente APC et la routine de saisie semi-automatique est appelée.

S’il n’existe aucune entrée dans la file d’attente APC, le thread est suspendu jusqu’à ce que l’attente soit satisfaite. L’attente peut être satisfaite en ajoutant une entrée à la file d’attente APC, par un délai d’attente ou par un handle qui devient signalé. Si l’attente est satisfaite par une entrée dans la file d’attente APC, le thread est réveillé et la routine d’achèvement est appelée. Dans ce cas, la valeur de retour de la fonction est l' **\_ \_ achèvement des e/s d’attente**.

Une fois la routine de saisie semi-automatique exécutée, le système recherche une autre entrée dans la file d’attente APC à traiter. Une fonction d’alerte ne retournera qu’une fois toutes les entrées APC traitées. Par conséquent, si des entrées sont ajoutées à la file d’attente APC plus rapidement qu’elles ne peuvent l’être, il est possible qu’un appel à une fonction d’alerte ne retourne jamais. Cela est tout particulièrement possible avec les minuteurs pouvant être attendus, si la période est plus petite que la durée nécessaire à l’exécution de la routine de saisie semi-automatique.

Lorsque vous utilisez un minuteur qui peut être utilisé avec un APC, le thread qui définit le minuteur ne doit pas attendre le handle de la minuterie. En procédant ainsi, vous faites en sorte que le thread se réveillera à la suite de l’ajout d’une entrée à la file d’attente APC. Par conséquent, le thread n’est plus dans un état d’alerte et la routine d’achèvement n’est pas appelée. Dans le code suivant, l’appel à [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) réveille le thread lorsqu’une entrée est ajoutée à la file d’attente APC du thread une fois que le minuteur est défini sur l’état signalé.


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’objets Timer Waitables](using-waitable-timer-objects.md)
</dt> </dl>

 

 
