---
description: Certains fichiers image contiennent des métadonnées que vous pouvez lire pour déterminer les fonctionnalités de l’image.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lecture et écriture de métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118294"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="227ac-103">Lecture et écriture de métadonnées</span><span class="sxs-lookup"><span data-stu-id="227ac-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="227ac-104">Certains fichiers image contiennent des métadonnées que vous pouvez lire pour déterminer les fonctionnalités de l’image.</span><span class="sxs-lookup"><span data-stu-id="227ac-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="227ac-105">Par exemple, une photographie numérique peut contenir des métadonnées que vous pouvez lire pour déterminer la marque et le modèle de l’appareil photo utilisé pour capturer l’image.</span><span class="sxs-lookup"><span data-stu-id="227ac-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="227ac-106">Avec Windows GDI+, vous pouvez lire les métadonnées existantes, et vous pouvez également écrire de nouvelles métadonnées dans des fichiers image.</span><span class="sxs-lookup"><span data-stu-id="227ac-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="227ac-107">GDI+ fournit un moyen uniforme de stocker et de récupérer des métadonnées à partir de fichiers image dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="227ac-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="227ac-108">Dans GDI+, une partie des métadonnées est appelée *élément de propriété*.</span><span class="sxs-lookup"><span data-stu-id="227ac-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="227ac-109">Vous pouvez stocker et récupérer des métadonnées en appelant les méthodes **SetPropertyItem** et **GetPropertyItem** de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , et vous n’avez pas à vous soucier des détails de la façon dont un format de fichier particulier stocke ces métadonnées.</span><span class="sxs-lookup"><span data-stu-id="227ac-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="227ac-110">GDI+ prend actuellement en charge les métadonnées pour les formats de fichier TIFF, JPEG, EXIF et PNG.</span><span class="sxs-lookup"><span data-stu-id="227ac-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="227ac-111">Le format Exif, qui spécifie comment stocker les images capturées par les appareils photo numériques, s’appuie sur les formats TIFF et JPEG.</span><span class="sxs-lookup"><span data-stu-id="227ac-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="227ac-112">EXIF utilise le format TIFF pour les données de pixels non compressées et le format JPEG pour les données de pixels compressés.</span><span class="sxs-lookup"><span data-stu-id="227ac-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="227ac-113">GDI+ définit un ensemble de balises de propriété qui identifient les éléments de propriété.</span><span class="sxs-lookup"><span data-stu-id="227ac-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="227ac-114">Certaines balises sont à usage général ; autrement dit, ils sont pris en charge par tous les formats de fichier mentionnés dans le paragraphe précédent.</span><span class="sxs-lookup"><span data-stu-id="227ac-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="227ac-115">Les autres balises sont à usage spécial et s’appliquent uniquement à certains formats.</span><span class="sxs-lookup"><span data-stu-id="227ac-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="227ac-116">Si vous essayez d’enregistrer un élément de propriété dans un fichier qui ne prend pas en charge cet élément de propriété, GDI+ ignore la demande.</span><span class="sxs-lookup"><span data-stu-id="227ac-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="227ac-117">Plus précisément, la méthode [**image :: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) retourne PropertyNotSupported.</span><span class="sxs-lookup"><span data-stu-id="227ac-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="227ac-118">Vous pouvez déterminer les éléments de propriété qui sont stockés dans un fichier image en appelant [**image :: GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span><span class="sxs-lookup"><span data-stu-id="227ac-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="227ac-119">Si vous essayez de récupérer un élément de propriété qui n’est pas dans le fichier, GDI+ ignore la demande.</span><span class="sxs-lookup"><span data-stu-id="227ac-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="227ac-120">Plus précisément, la méthode [**image :: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) retourne PropertyNotFound.</span><span class="sxs-lookup"><span data-stu-id="227ac-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="227ac-121">Lecture des métadonnées d’un fichier</span><span class="sxs-lookup"><span data-stu-id="227ac-121">Reading Metadata from a File</span></span>

<span data-ttu-id="227ac-122">L’application console suivante appelle la méthode **GetPropertySize** d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) pour déterminer le nombre de portions de métadonnées dans le fichier FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="227ac-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="227ac-123">Le code précédent, ainsi qu’un fichier particulier, FakePhoto.jpg, ont produit la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="227ac-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="227ac-124">GDI+ stocke un élément de métadonnées individuel dans un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .</span><span class="sxs-lookup"><span data-stu-id="227ac-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="227ac-125">Vous pouvez appeler la méthode **GetAllPropertyItems** de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) pour récupérer toutes les métadonnées d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="227ac-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="227ac-126">La méthode **GetAllPropertyItems** retourne un tableau d’objets **PropertyItem** .</span><span class="sxs-lookup"><span data-stu-id="227ac-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="227ac-127">Avant d’appeler **GetAllPropertyItems**, vous devez allouer une mémoire tampon suffisamment grande pour recevoir ce tableau.</span><span class="sxs-lookup"><span data-stu-id="227ac-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="227ac-128">Vous pouvez appeler la méthode **GetPropertySize** de la classe **image** pour connaître la taille (en octets) de la mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="227ac-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="227ac-129">Un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) contient les quatre membres publics suivants :</span><span class="sxs-lookup"><span data-stu-id="227ac-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            | <span data-ttu-id="227ac-130">Description</span><span class="sxs-lookup"><span data-stu-id="227ac-130">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="227ac-131">**id**</span><span class="sxs-lookup"><span data-stu-id="227ac-131">**id**</span></span>     | <span data-ttu-id="227ac-132">Balise qui identifie l’élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="227ac-132">A tag that identifies the metadata item.</span></span> <span data-ttu-id="227ac-133">Les valeurs qui peuvent être assignées à **ID** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime et like) sont définies dans Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="227ac-133">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="227ac-134">**length**</span><span class="sxs-lookup"><span data-stu-id="227ac-134">**length**</span></span> | <span data-ttu-id="227ac-135">Longueur, en octets, du tableau de valeurs vers lequel pointe la **valeur** du membre de données.</span><span class="sxs-lookup"><span data-stu-id="227ac-135">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="227ac-136">Notez que si le membre de données de **type** est défini sur PropertyTagTypeASCII, le membre de données de longueur est la **longueur** d’une chaîne de caractères se terminant par un caractère null, y compris la marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="227ac-136">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="227ac-137">**type**</span><span class="sxs-lookup"><span data-stu-id="227ac-137">**type**</span></span>   | <span data-ttu-id="227ac-138">Type de données des valeurs du tableau vers lequel pointe la valeur du membre de données.</span><span class="sxs-lookup"><span data-stu-id="227ac-138">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="227ac-139">Les constantes (PropertyTagTypeByte, PropertyTagTypeASCII et like) qui représentent différents types de données sont décrites dans [**constantes de type de balise de propriété d’image**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="227ac-139">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="227ac-140">**value**</span><span class="sxs-lookup"><span data-stu-id="227ac-140">**value**</span></span>  | <span data-ttu-id="227ac-141">Pointeur vers un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="227ac-141">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="227ac-142">L’application console suivante lit et affiche les sept éléments de métadonnées dans le fichier FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="227ac-142">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="227ac-143">La fonction main repose sur la fonction d’assistance PropertyTypeFromWORD, qui est illustrée à la suite de la fonction main.</span><span class="sxs-lookup"><span data-stu-id="227ac-143">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



<span data-ttu-id="227ac-144">L’application console précédente génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="227ac-144">The preceding console application produces the following output:</span></span>


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



<span data-ttu-id="227ac-145">La sortie précédente montre un numéro d’ID hexadécimal pour chaque élément de propriété.</span><span class="sxs-lookup"><span data-stu-id="227ac-145">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="227ac-146">Vous pouvez rechercher ces numéros d’identification dans les [constantes de balise de propriété d’image](-gdiplus-constant-image-property-tag-constants.md) et savoir qu’ils représentent les balises de propriété suivantes.</span><span class="sxs-lookup"><span data-stu-id="227ac-146">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="227ac-147">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="227ac-147">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="227ac-148">Balise de propriété</span><span class="sxs-lookup"><span data-stu-id="227ac-148">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="227ac-149">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="227ac-149">0x0320 0x010f</span></span><br/>  <span data-ttu-id="227ac-150">0x0110</span><span class="sxs-lookup"><span data-stu-id="227ac-150">0x0110</span></span><br/>  <span data-ttu-id="227ac-151">0x9003</span><span class="sxs-lookup"><span data-stu-id="227ac-151">0x9003</span></span><br/>  <span data-ttu-id="227ac-152">0x829a</span><span class="sxs-lookup"><span data-stu-id="227ac-152">0x829a</span></span><br/>  <span data-ttu-id="227ac-153">0x5090</span><span class="sxs-lookup"><span data-stu-id="227ac-153">0x5090</span></span><br/>  <span data-ttu-id="227ac-154">0x5091</span><span class="sxs-lookup"><span data-stu-id="227ac-154">0x5091</span></span><br/> | <span data-ttu-id="227ac-155">PropertyTagImageTitle PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="227ac-155">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="227ac-156">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="227ac-156">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="227ac-157">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="227ac-157">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="227ac-158">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="227ac-158">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="227ac-159">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="227ac-159">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="227ac-160">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="227ac-160">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="227ac-161">Le deuxième élément de la propriété (index 1) de la liste a l' **ID** PropertyTagEquipMake et le **type** PropertyTagTypeASCII.</span><span class="sxs-lookup"><span data-stu-id="227ac-161">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="227ac-162">L’exemple suivant, qui est la continuation de l’application console précédente, affiche la valeur de cet élément de propriété :</span><span class="sxs-lookup"><span data-stu-id="227ac-162">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="227ac-163">La ligne de code précédente produit la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="227ac-163">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="227ac-164">Le cinquième élément de la propriété (index 4) de la liste porte l' **ID** PropertyTagExifExposureTime et le **type** PropertyTagTypeRational.</span><span class="sxs-lookup"><span data-stu-id="227ac-164">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="227ac-165">Ce type de données (PropertyTagTypeRational) est une paire de **longues** s.</span><span class="sxs-lookup"><span data-stu-id="227ac-165">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="227ac-166">L’exemple suivant, qui est la continuation de l’application console précédente, affiche ces deux valeurs **longues** sous la forme d’une fraction.</span><span class="sxs-lookup"><span data-stu-id="227ac-166">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="227ac-167">Cette fraction, 1/125, est le temps d’exposition mesuré en secondes.</span><span class="sxs-lookup"><span data-stu-id="227ac-167">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="227ac-168">Le code ci-dessus génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="227ac-168">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="227ac-169">Écriture de métadonnées dans un fichier</span><span class="sxs-lookup"><span data-stu-id="227ac-169">Writing Metadata to a File</span></span>

<span data-ttu-id="227ac-170">Pour écrire un élément de métadonnées dans un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , initialisez un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , puis transmettez l’adresse de cet objet **PropertyItem** à la méthode **SetPropertyItem** de l’objet **image** .</span><span class="sxs-lookup"><span data-stu-id="227ac-170">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="227ac-171">L’application console suivante écrit un élément (le titre de l’image) des métadonnées dans un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , puis enregistre l’image dans le fichier disque FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="227ac-171">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="227ac-172">La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans la rubrique [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="227ac-172">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
