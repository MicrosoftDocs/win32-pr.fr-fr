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
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="f0427-103">Comment traiter la notification au \_ format DTN</span><span class="sxs-lookup"><span data-stu-id="f0427-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="f0427-104">Cette rubrique montre comment traiter une notification de format envoyée par le contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="f0427-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f0427-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="f0427-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f0427-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="f0427-106">Technologies</span></span>

-   [<span data-ttu-id="f0427-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="f0427-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f0427-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f0427-108">Prerequisites</span></span>

-   <span data-ttu-id="f0427-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="f0427-109">C/C++</span></span>
-   <span data-ttu-id="f0427-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="f0427-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f0427-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="f0427-111">Instructions</span></span>


<span data-ttu-id="f0427-112">Un contrôle de PAO envoie la notification de [ \_ format DTN](dtn-format.md) au texte de la requête qui sera affiché dans un champ de rappel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f0427-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="f0427-113">Votre application doit gérer cette notification pour permettre au contrôle de PAO d’afficher des informations qu’il ne prend pas en charge de manière native.</span><span class="sxs-lookup"><span data-stu-id="f0427-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="f0427-114">L’exemple de code C++ suivant est une fonction définie par l’application (**format**) qui traite les codes de notification de [ \_ format DTN](dtn-format.md) en fournissant une chaîne de texte pour un champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="f0427-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="f0427-115">L’application appelle la fonction **GetDayNum** définie par l’application pour demander le nombre de jours à utiliser dans la chaîne de rappel.</span><span class="sxs-lookup"><span data-stu-id="f0427-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


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



<span data-ttu-id="f0427-116">**La fonction GetDayNum définie par l’application**</span><span class="sxs-lookup"><span data-stu-id="f0427-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="f0427-117">L’exemple de fonction de fonction définie par l' **application appelle la fonction** **GetDayNum** définie par l’application suivante pour demander le numéro de jour en fonction de la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="f0427-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="f0427-118">**GetDayNum** retourne une valeur **int** qui représente le jour actuel de l’année, de 0 à 366.</span><span class="sxs-lookup"><span data-stu-id="f0427-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="f0427-119">Cette fonction appelle une autre fonction définie par l’application, **IsLeapYr**, pendant le traitement.</span><span class="sxs-lookup"><span data-stu-id="f0427-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


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



<span data-ttu-id="f0427-120">**La fonction IsLeapYr définie par l’application**</span><span class="sxs-lookup"><span data-stu-id="f0427-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="f0427-121">La fonction définie par l’application **GetDayNum** appelle la fonction **IsLeapYr** pour déterminer si l’année en cours est une année bissextile.</span><span class="sxs-lookup"><span data-stu-id="f0427-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="f0427-122">**IsLeapYr** retourne une valeur **booléenne** **true** s’il s’agit d’une année bissextile et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f0427-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f0427-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0427-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0427-124">Utilisation des contrôles de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="f0427-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="f0427-125">Référence de contrôle de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="f0427-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f0427-126">Sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="f0427-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




