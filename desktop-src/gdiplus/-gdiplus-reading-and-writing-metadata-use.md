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
# <a name="reading-and-writing-metadata"></a>Lecture et écriture de métadonnées

Certains fichiers image contiennent des métadonnées que vous pouvez lire pour déterminer les fonctionnalités de l’image. Par exemple, une photographie numérique peut contenir des métadonnées que vous pouvez lire pour déterminer la marque et le modèle de l’appareil photo utilisé pour capturer l’image. Avec Windows GDI+, vous pouvez lire les métadonnées existantes, et vous pouvez également écrire de nouvelles métadonnées dans des fichiers image.

GDI+ fournit un moyen uniforme de stocker et de récupérer des métadonnées à partir de fichiers image dans différents formats. Dans GDI+, une partie des métadonnées est appelée *élément de propriété*. Vous pouvez stocker et récupérer des métadonnées en appelant les méthodes **SetPropertyItem** et **GetPropertyItem** de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , et vous n’avez pas à vous soucier des détails de la façon dont un format de fichier particulier stocke ces métadonnées.

GDI+ prend actuellement en charge les métadonnées pour les formats de fichier TIFF, JPEG, EXIF et PNG. Le format Exif, qui spécifie comment stocker les images capturées par les appareils photo numériques, s’appuie sur les formats TIFF et JPEG. EXIF utilise le format TIFF pour les données de pixels non compressées et le format JPEG pour les données de pixels compressés.

GDI+ définit un ensemble de balises de propriété qui identifient les éléments de propriété. Certaines balises sont à usage général ; autrement dit, ils sont pris en charge par tous les formats de fichier mentionnés dans le paragraphe précédent. Les autres balises sont à usage spécial et s’appliquent uniquement à certains formats. Si vous essayez d’enregistrer un élément de propriété dans un fichier qui ne prend pas en charge cet élément de propriété, GDI+ ignore la demande. Plus précisément, la méthode [**image :: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) retourne PropertyNotSupported.

Vous pouvez déterminer les éléments de propriété qui sont stockés dans un fichier image en appelant [**image :: GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist). Si vous essayez de récupérer un élément de propriété qui n’est pas dans le fichier, GDI+ ignore la demande. Plus précisément, la méthode [**image :: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) retourne PropertyNotFound.

## <a name="reading-metadata-from-a-file"></a>Lecture des métadonnées d’un fichier

L’application console suivante appelle la méthode **GetPropertySize** d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) pour déterminer le nombre de portions de métadonnées dans le fichier FakePhoto.jpg.


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



Le code précédent, ainsi qu’un fichier particulier, FakePhoto.jpg, ont produit la sortie suivante :


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI+ stocke un élément de métadonnées individuel dans un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) . Vous pouvez appeler la méthode **GetAllPropertyItems** de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) pour récupérer toutes les métadonnées d’un fichier. La méthode **GetAllPropertyItems** retourne un tableau d’objets **PropertyItem** . Avant d’appeler **GetAllPropertyItems**, vous devez allouer une mémoire tampon suffisamment grande pour recevoir ce tableau. Vous pouvez appeler la méthode **GetPropertySize** de la classe **image** pour connaître la taille (en octets) de la mémoire tampon requise.

Un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) contient les quatre membres publics suivants :



|            | Description                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | Balise qui identifie l’élément de métadonnées. Les valeurs qui peuvent être assignées à **ID** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime et like) sont définies dans Gdiplusimaging. h.                                                                                           |
| **length** | Longueur, en octets, du tableau de valeurs vers lequel pointe la **valeur** du membre de données. Notez que si le membre de données de **type** est défini sur PropertyTagTypeASCII, le membre de données de longueur est la **longueur** d’une chaîne de caractères se terminant par un caractère null, y compris la marque de fin null.                        |
| **type**   | Type de données des valeurs du tableau vers lequel pointe la valeur du membre de données. Les constantes (PropertyTagTypeByte, PropertyTagTypeASCII et like) qui représentent différents types de données sont décrites dans [**constantes de type de balise de propriété d’image**](-gdiplus-constant-image-property-tag-type-constants.md). |
| **value**  | Pointeur vers un tableau de valeurs.                                                                                                                                                                                                                                                                       |



 

L’application console suivante lit et affiche les sept éléments de métadonnées dans le fichier FakePhoto.jpg. La fonction main repose sur la fonction d’assistance PropertyTypeFromWORD, qui est illustrée à la suite de la fonction main.


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



L’application console précédente génère la sortie suivante :


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



La sortie précédente montre un numéro d’ID hexadécimal pour chaque élément de propriété. Vous pouvez rechercher ces numéros d’identification dans les [constantes de balise de propriété d’image](-gdiplus-constant-image-property-tag-constants.md) et savoir qu’ils représentent les balises de propriété suivantes.



| Valeur hexadécimale                                                                                                       | Balise de propriété                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010f<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | PropertyTagImageTitle PropertyTagEquipMake<br/>  PropertyTagEquipModel<br/>  PropertyTagExifDTOriginal<br/>  PropertyTagExifExposureTime<br/>  PropertyTagLuminanceTable<br/>  PropertyTagChrominanceTable<br/> |



 

Le deuxième élément de la propriété (index 1) de la liste a l' **ID** PropertyTagEquipMake et le **type** PropertyTagTypeASCII. L’exemple suivant, qui est la continuation de l’application console précédente, affiche la valeur de cet élément de propriété :


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



La ligne de code précédente produit la sortie suivante :


```
The equipment make is Northwind Traders.
```



Le cinquième élément de la propriété (index 4) de la liste porte l' **ID** PropertyTagExifExposureTime et le **type** PropertyTagTypeRational. Ce type de données (PropertyTagTypeRational) est une paire de **longues** s. L’exemple suivant, qui est la continuation de l’application console précédente, affiche ces deux valeurs **longues** sous la forme d’une fraction. Cette fraction, 1/125, est le temps d’exposition mesuré en secondes.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



Le code ci-dessus génère la sortie suivante :


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Écriture de métadonnées dans un fichier

Pour écrire un élément de métadonnées dans un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , initialisez un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , puis transmettez l’adresse de cet objet **PropertyItem** à la méthode **SetPropertyItem** de l’objet **image** .

L’application console suivante écrit un élément (le titre de l’image) des métadonnées dans un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , puis enregistre l’image dans le fichier disque FakePhoto2.jpg. La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans la rubrique [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



 

 
