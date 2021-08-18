---
description: La classe la hérite de la classe de base abstraite FontCollection. Vous pouvez utiliser un objet la pour conserver un ensemble de polices spécifiquement pour votre application.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Création de collections de polices privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df673273611ed329e933c84e6540ed984088202590dc1d1c644ccdedca2c80c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977589"
---
# <a name="creating-a-private-font-collection"></a>Création de collections de polices privées

La classe [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) hérite de la classe de base abstraite [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . Vous pouvez utiliser un objet **la** pour conserver un ensemble de polices spécifiquement pour votre application.

Une collection de polices privée peut inclure des polices système installées, ainsi que des polices qui n’ont pas été installées sur l’ordinateur. Pour ajouter un fichier de polices à une collection de polices privées, appelez la méthode [**la :: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) d’un objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .

> [!Note]  
> lorsque vous utilisez l’API GDI+, vous ne devez jamais autoriser votre application à télécharger des polices arbitraires à partir de sources non approuvées. Le système d’exploitation requiert des privilèges élevés pour s’assurer que toutes les polices installées sont approuvées.

 

La méthode [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) d’un objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) retourne un tableau d’objets [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Avant d’appeler **FontCollection :: GetFamilies**, vous devez allouer une mémoire tampon suffisamment grande pour contenir ce tableau. Pour déterminer la taille de la mémoire tampon requise, appelez la méthode [**FontCollection :: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) et multipliez la valeur de retour par **sizeof**(**FontFamily**).

Le nombre de familles de polices dans une collection de polices privées n’est pas nécessairement le même que le nombre de fichiers de polices qui ont été ajoutés à la collection. Par exemple, supposons que vous ajoutiez les fichiers ArialBd. tff, Times. TFF et TimesBd. tff à une collection. Il y aura trois fichiers, mais seulement deux familles dans la collection, car Times. TFF et TimesBd. tff appartiennent à la même famille.

L’exemple suivant ajoute les trois fichiers de police suivants à un objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :

-   C : \\ winnt \\ polices \\ Arial. tff (Arial, Regular)
-   C : \\ winnt \\ polices \\ CourBI. tff (Courier New, Bold italique)
-   C : \\ winnt \\ polices \\ TimesBd. tff (Times New Roman, gras)

Le code appelle la méthode [**FontCollection :: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) de l’objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) pour déterminer le nombre de familles dans la collection privée, puis appelle [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) pour récupérer un tableau d’objets [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .

Pour chaque objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) de la collection, le code appelle la méthode [**FontFamily :: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) pour déterminer si divers styles (normal, gras, italique, gras italique, souligné et barré) sont disponibles. Les arguments passés à la méthode **FontFamily :: IsStyleAvailable** sont des membres de l’énumération [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , qui est déclarée dans Gdiplusenums. h.

Si une combinaison famille/style particulière est disponible, un objet [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) est construit à l’aide de cette famille et de ce style. Le premier argument passé au constructeur **font** est le nom de famille de polices (et non un objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) comme c’est le cas pour les autres variations du constructeur **font** ) et le dernier argument est l’adresse de l’objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) . Une fois que l’objet **font** est construit, son adresse est transmise à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour afficher le nom de famille, ainsi que le nom du style.


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



L’illustration suivante montre la sortie du code précédent.

![capture d’écran d’une fenêtre qui répertorie neuf noms de police, chacun d’entre eux montrant la police nommée](images/fontstext7.png)

Arial. tff (qui a été ajouté à la collection de polices privée dans l’exemple de code précédent) est le fichier de police pour le style Arial Regular. Notez, cependant, que la sortie du programme affiche plusieurs styles disponibles autres que normal pour la famille de polices Arial. cela est dû au fait que Windows GDI+ peut simuler les styles italiques gras, italique et gras à partir du style normal. GDI+ pouvez également produire des soulignements et des strikeouts à partir du style normal.

de même, GDI+ peut simuler le style italique gras à partir du style gras ou du style italique. La sortie du programme indique que le style italique gras est disponible pour la famille Times, même si TimesBd. tff (Times New Roman, Bold) est le seul fichier dans la collection.

ce tableau spécifie les polices non-système prises en charge par GDI+.



|                     | GDI | GDI+ sur Windows 7 | GDI+ sur Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . FON                | oui | non                | non                | non          |
| . FNT                | oui | non                | non                | non          |
| . TTF                | oui | oui               | oui               | oui         |
| . OTF avec TrueType  | oui | oui               | oui               | oui         |
| . OTF avec Adobe CFF | oui | non                | oui               | oui         |
| Adobe type 1        | oui | non                | non                | non          |



 

 

 



