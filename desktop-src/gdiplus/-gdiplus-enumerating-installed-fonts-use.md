---
description: La classe InstalledFontCollection hérite de la classe de base abstraite FontCollection.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Énumération des polices installées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa54298cb7d177708d609e2ee011dd4da7173c726445b59b07a9c8e60ce786cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067350"
---
# <a name="enumerating-installed-fonts"></a>Énumération des polices installées

La classe [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) hérite de la classe de base abstraite [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . Vous pouvez utiliser un objet **InstalledFontCollection** pour énumérer les polices installées sur l’ordinateur. La méthode [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) d’un objet **InstalledFontCollection** retourne un tableau d’objets [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Avant d’appeler **FontCollection :: GetFamilies**, vous devez allouer une mémoire tampon suffisamment grande pour contenir ce tableau. Pour déterminer la taille de la mémoire tampon requise, appelez la méthode [**FontCollection :: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) et multipliez la valeur de retour par **sizeof**(**FontFamily**).

L’exemple suivant répertorie les noms de toutes les familles de polices installées sur l’ordinateur. Le code récupère les noms des familles de polices en appelant la méthode [**FontFamily :: GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) de chaque objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) dans le tableau retourné par [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies). À mesure que les noms de famille sont récupérés, ils sont concaténés pour former une liste séparée par des virgules. Ensuite, la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dessine la liste séparée par des virgules dans un rectangle.


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



L’illustration suivante montre une sortie possible du code précédent. Si vous exécutez le code, la sortie peut être différente, selon les polices installées sur votre ordinateur.

![capture d’écran d’une fenêtre contenant une liste séparée par des virgules de familles de polices installées](images/fontstext6.png)

 

 



