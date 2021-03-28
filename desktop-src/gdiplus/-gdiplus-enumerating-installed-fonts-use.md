---
description: La classe InstalledFontCollection hérite de la classe de base abstraite FontCollection.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Énumération des polices installées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202424"
---
# <a name="enumerating-installed-fonts"></a><span data-ttu-id="ea913-103">Énumération des polices installées</span><span class="sxs-lookup"><span data-stu-id="ea913-103">Enumerating Installed Fonts</span></span>

<span data-ttu-id="ea913-104">La classe [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) hérite de la classe de base abstraite [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="ea913-104">The [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="ea913-105">Vous pouvez utiliser un objet **InstalledFontCollection** pour énumérer les polices installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ea913-105">You can use an **InstalledFontCollection** object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="ea913-106">La méthode [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) d’un objet **InstalledFontCollection** retourne un tableau d’objets [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="ea913-106">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of an **InstalledFontCollection** object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="ea913-107">Avant d’appeler **FontCollection :: GetFamilies**, vous devez allouer une mémoire tampon suffisamment grande pour contenir ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ea913-107">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="ea913-108">Pour déterminer la taille de la mémoire tampon requise, appelez la méthode [**FontCollection :: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) et multipliez la valeur de retour par **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="ea913-108">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="ea913-109">L’exemple suivant répertorie les noms de toutes les familles de polices installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ea913-109">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="ea913-110">Le code récupère les noms des familles de polices en appelant la méthode [**FontFamily :: GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) de chaque objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) dans le tableau retourné par [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span><span class="sxs-lookup"><span data-stu-id="ea913-110">The code retrieves the font family names by calling the [**FontFamily::GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) method of each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the array returned by [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span></span> <span data-ttu-id="ea913-111">À mesure que les noms de famille sont récupérés, ils sont concaténés pour former une liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ea913-111">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="ea913-112">Ensuite, la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dessine la liste séparée par des virgules dans un rectangle.</span><span class="sxs-lookup"><span data-stu-id="ea913-112">Then the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class draws the comma-separated list in a rectangle.</span></span>


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



<span data-ttu-id="ea913-113">L’illustration suivante montre une sortie possible du code précédent.</span><span class="sxs-lookup"><span data-stu-id="ea913-113">The following illustration shows a possible output of the preceding code.</span></span> <span data-ttu-id="ea913-114">Si vous exécutez le code, la sortie peut être différente, selon les polices installées sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ea913-114">If you run the code, the output might be different, depending on the fonts installed on your computer.</span></span>

![capture d’écran d’une fenêtre contenant une liste séparée par des virgules de familles de polices installées](images/fontstext6.png)

 

 



