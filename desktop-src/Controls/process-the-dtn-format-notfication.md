---
title: Comment traiter la notification de DTN_FORMAT
description: Cette rubrique montre comment traiter une notification de format envoyée par le contrôle de sélecteur de dates et d’heures (PAO).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842894"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Comment traiter la notification au \_ format DTN

Cette rubrique montre comment traiter une notification de format envoyée par le contrôle de sélecteur de dates et d’heures (PAO).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Un contrôle de PAO envoie la notification de [ \_ format DTN](dtn-format.md) au texte de la requête qui sera affiché dans un champ de rappel du contrôle. Votre application doit gérer cette notification pour permettre au contrôle de PAO d’afficher des informations qu’il ne prend pas en charge de manière native.

L’exemple de code C++ suivant est une fonction définie par l’application (**format**) qui traite les codes de notification de [ \_ format DTN](dtn-format.md) en fournissant une chaîne de texte pour un champ de rappel. L’application appelle la fonction **GetDayNum** définie par l’application pour demander le nombre de jours à utiliser dans la chaîne de rappel.


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



**La fonction GetDayNum définie par l’application**

L’exemple de fonction de fonction définie par l' **application appelle la fonction** **GetDayNum** définie par l’application suivante pour demander le numéro de jour en fonction de la date actuelle. **GetDayNum** retourne une valeur **int** qui représente le jour actuel de l’année, de 0 à 366. Cette fonction appelle une autre fonction définie par l’application, **IsLeapYr**, pendant le traitement.


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



**La fonction IsLeapYr définie par l’application**

La fonction définie par l’application **GetDayNum** appelle la fonction **IsLeapYr** pour déterminer si l’année en cours est une année bissextile. **IsLeapYr** retourne une valeur **booléenne** **true** s’il s’agit d’une année bissextile et **false** dans le cas contraire.


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
}        
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles de sélecteur de date et heure](using-date-and-time-picker.md)
</dt> <dt>

[Référence de contrôle de sélecteur de date et heure](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Sélecteur de date et heure](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




