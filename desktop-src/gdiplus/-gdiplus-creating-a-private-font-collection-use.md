---
description: La classe la hérite de la classe de base abstraite FontCollection. Vous pouvez utiliser un objet la pour conserver un ensemble de polices spécifiquement pour votre application.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Création de collections de polices privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202429"
---
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="2b3ed-104">Création de collections de polices privées</span><span class="sxs-lookup"><span data-stu-id="2b3ed-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="2b3ed-105">La classe [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) hérite de la classe de base abstraite [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="2b3ed-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="2b3ed-106">Vous pouvez utiliser un objet **la** pour conserver un ensemble de polices spécifiquement pour votre application.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="2b3ed-107">Une collection de polices privée peut inclure des polices système installées, ainsi que des polices qui n’ont pas été installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="2b3ed-108">Pour ajouter un fichier de polices à une collection de polices privées, appelez la méthode [**la :: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) d’un objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="2b3ed-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="2b3ed-109">Lorsque vous utilisez l’API GDI+, vous ne devez jamais autoriser votre application à télécharger des polices arbitraires à partir de sources non approuvées.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="2b3ed-110">Le système d’exploitation requiert des privilèges élevés pour s’assurer que toutes les polices installées sont approuvées.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="2b3ed-111">La méthode [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) d’un objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) retourne un tableau d’objets [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="2b3ed-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="2b3ed-112">Avant d’appeler **FontCollection :: GetFamilies**, vous devez allouer une mémoire tampon suffisamment grande pour contenir ce tableau.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="2b3ed-113">Pour déterminer la taille de la mémoire tampon requise, appelez la méthode [**FontCollection :: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) et multipliez la valeur de retour par **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="2b3ed-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="2b3ed-114">Le nombre de familles de polices dans une collection de polices privées n’est pas nécessairement le même que le nombre de fichiers de polices qui ont été ajoutés à la collection.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="2b3ed-115">Par exemple, supposons que vous ajoutiez les fichiers ArialBd. tff, Times. TFF et TimesBd. tff à une collection.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="2b3ed-116">Il y aura trois fichiers, mais seulement deux familles dans la collection, car Times. TFF et TimesBd. tff appartiennent à la même famille.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="2b3ed-117">L’exemple suivant ajoute les trois fichiers de police suivants à un objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :</span><span class="sxs-lookup"><span data-stu-id="2b3ed-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="2b3ed-118">C : \\ winnt \\ polices \\ Arial. tff (Arial, Regular)</span><span class="sxs-lookup"><span data-stu-id="2b3ed-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="2b3ed-119">C : \\ winnt \\ polices \\ CourBI. tff (Courier New, Bold italique)</span><span class="sxs-lookup"><span data-stu-id="2b3ed-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="2b3ed-120">C : \\ winnt \\ polices \\ TimesBd. tff (Times New Roman, gras)</span><span class="sxs-lookup"><span data-stu-id="2b3ed-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="2b3ed-121">Le code appelle la méthode [**FontCollection :: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) de l’objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) pour déterminer le nombre de familles dans la collection privée, puis appelle [**FontCollection :: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) pour récupérer un tableau d’objets [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="2b3ed-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="2b3ed-122">Pour chaque objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) de la collection, le code appelle la méthode [**FontFamily :: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) pour déterminer si divers styles (normal, gras, italique, gras italique, souligné et barré) sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="2b3ed-123">Les arguments passés à la méthode **FontFamily :: IsStyleAvailable** sont des membres de l’énumération [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , qui est déclarée dans Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="2b3ed-124">Si une combinaison famille/style particulière est disponible, un objet [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) est construit à l’aide de cette famille et de ce style.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="2b3ed-125">Le premier argument passé au constructeur **font** est le nom de famille de polices (et non un objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) comme c’est le cas pour les autres variations du constructeur **font** ) et le dernier argument est l’adresse de l’objet [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="2b3ed-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="2b3ed-126">Une fois que l’objet **font** est construit, son adresse est transmise à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour afficher le nom de famille, ainsi que le nom du style.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


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



<span data-ttu-id="2b3ed-127">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-127">The following illustration shows the output of the preceding code.</span></span>

![capture d’écran d’une fenêtre qui répertorie neuf noms de police, chacun d’entre eux montrant la police nommée](images/fontstext7.png)

<span data-ttu-id="2b3ed-129">Arial. tff (qui a été ajouté à la collection de polices privée dans l’exemple de code précédent) est le fichier de police pour le style Arial Regular.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="2b3ed-130">Notez, cependant, que la sortie du programme affiche plusieurs styles disponibles autres que normal pour la famille de polices Arial.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="2b3ed-131">Cela est dû au fait que Windows GDI+ peut simuler les styles italiques gras, italique et gras à partir du style normal.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="2b3ed-132">GDI+ peut également produire des soulignements et des strikeouts à partir du style normal.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="2b3ed-133">De même, GDI+ peut simuler le style italique gras à partir du style gras ou du style italique.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="2b3ed-134">La sortie du programme indique que le style italique gras est disponible pour la famille Times, même si TimesBd. tff (Times New Roman, Bold) est le seul fichier dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="2b3ed-135">Ce tableau spécifie les polices non-système prises en charge par GDI+.</span><span class="sxs-lookup"><span data-stu-id="2b3ed-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="2b3ed-136">GDI</span><span class="sxs-lookup"><span data-stu-id="2b3ed-136">GDI</span></span> | <span data-ttu-id="2b3ed-137">GDI+ sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b3ed-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="2b3ed-138">GDI+ sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="2b3ed-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="2b3ed-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="2b3ed-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="2b3ed-140">. FON</span><span class="sxs-lookup"><span data-stu-id="2b3ed-140">.FON</span></span>                | <span data-ttu-id="2b3ed-141">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-141">yes</span></span> | <span data-ttu-id="2b3ed-142">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-142">no</span></span>                | <span data-ttu-id="2b3ed-143">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-143">no</span></span>                | <span data-ttu-id="2b3ed-144">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-144">no</span></span>          |
| <span data-ttu-id="2b3ed-145">. FNT</span><span class="sxs-lookup"><span data-stu-id="2b3ed-145">.FNT</span></span>                | <span data-ttu-id="2b3ed-146">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-146">yes</span></span> | <span data-ttu-id="2b3ed-147">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-147">no</span></span>                | <span data-ttu-id="2b3ed-148">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-148">no</span></span>                | <span data-ttu-id="2b3ed-149">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-149">no</span></span>          |
| <span data-ttu-id="2b3ed-150">. TTF</span><span class="sxs-lookup"><span data-stu-id="2b3ed-150">.TTF</span></span>                | <span data-ttu-id="2b3ed-151">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-151">yes</span></span> | <span data-ttu-id="2b3ed-152">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-152">yes</span></span>               | <span data-ttu-id="2b3ed-153">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-153">yes</span></span>               | <span data-ttu-id="2b3ed-154">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-154">yes</span></span>         |
| <span data-ttu-id="2b3ed-155">. OTF avec TrueType</span><span class="sxs-lookup"><span data-stu-id="2b3ed-155">.OTF with TrueType</span></span>  | <span data-ttu-id="2b3ed-156">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-156">yes</span></span> | <span data-ttu-id="2b3ed-157">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-157">yes</span></span>               | <span data-ttu-id="2b3ed-158">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-158">yes</span></span>               | <span data-ttu-id="2b3ed-159">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-159">yes</span></span>         |
| <span data-ttu-id="2b3ed-160">. OTF avec Adobe CFF</span><span class="sxs-lookup"><span data-stu-id="2b3ed-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="2b3ed-161">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-161">yes</span></span> | <span data-ttu-id="2b3ed-162">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-162">no</span></span>                | <span data-ttu-id="2b3ed-163">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-163">yes</span></span>               | <span data-ttu-id="2b3ed-164">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-164">yes</span></span>         |
| <span data-ttu-id="2b3ed-165">Adobe type 1</span><span class="sxs-lookup"><span data-stu-id="2b3ed-165">Adobe Type 1</span></span>        | <span data-ttu-id="2b3ed-166">Oui</span><span class="sxs-lookup"><span data-stu-id="2b3ed-166">yes</span></span> | <span data-ttu-id="2b3ed-167">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-167">no</span></span>                | <span data-ttu-id="2b3ed-168">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-168">no</span></span>                | <span data-ttu-id="2b3ed-169">non</span><span class="sxs-lookup"><span data-stu-id="2b3ed-169">no</span></span>          |



 

 

 



