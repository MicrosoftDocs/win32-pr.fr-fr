---
description: L’application console suivante répertorie tous les paramètres pris en charge par les différents encodeurs installés sur l’ordinateur.
ms.assetid: c80ad013-0b92-461f-8714-4b6d0cb6de0d
title: Liste des paramètres et des valeurs pour tous les encodeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdaf522193f1074a28fe9f5ebb8a7afc2bade0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012426"
---
# <a name="listing-parameters-and-values-for-all-encoders"></a>Liste des paramètres et des valeurs pour tous les encodeurs

L’application console suivante répertorie tous les paramètres pris en charge par les différents encodeurs installés sur l’ordinateur. La fonction main appelle [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) pour découvrir quels encodeurs sont disponibles. Pour chaque encodeur disponible, la fonction main appelle la fonction d’assistance ShowAllEncoderParameters.

La fonction ShowAllEncoderParameters appelle la méthode [**image :: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) pour découvrir quels paramètres sont pris en charge par un encodeur donné. Pour chaque paramètre pris en charge, la fonction répertorie la catégorie, le type de données et le nombre de valeurs. La fonction ShowAllEncoderParameters s’appuie sur deux fonctions d’assistance : EncoderParameterCategoryFromGUID et ValueTypeFromULONG.


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

// Helper functions
void ShowAllEncoderParameters(ImageCodecInfo*);
HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars);
HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars);

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // Number of image encoders
   UINT  size;       // Size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfos, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);
    
   // For each ImageCodecInfo object in the array, show all parameters.
   for(UINT j = 0; j < num; ++j)
   { 
      ShowAllEncoderParameters(&(pImageCodecInfo[j]));
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}


/////////////////////////////////////////////////
// Helper functions

VOID ShowAllEncoderParameters(ImageCodecInfo* pImageCodecInfo)
{
   CONST MAX_CATEGORY_LENGTH = 50;
   CONST MAX_VALUE_TYPE_LENGTH = 50;
   WCHAR strParameterCategory[MAX_CATEGORY_LENGTH] = L"";
   WCHAR strValueType[MAX_VALUE_TYPE_LENGTH] = L"";

   wprintf(L"\n\n%s\n", pImageCodecInfo->MimeType);

   // Create a Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap bitmap(1, 1);

   // How big (in bytes) is the encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap.GetEncoderParameterListSize(&pImageCodecInfo->Clsid);
   printf("  The parameter list requires %d bytes.\n", listSize);

   if(listSize == 0)
      return;

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   if(pEncoderParameters == NULL)
      return;

   // Get the parameter list for the encoder.
   bitmap.GetEncoderParameterList(
      &pImageCodecInfo->Clsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("  There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   // For each EncoderParameter object in the array, list the
   // parameter category, data type, and number of values.
   for(UINT k = 0; k < pEncoderParameters->Count; ++k)
   {
      EncoderParameterCategoryFromGUID(
         pEncoderParameters->Parameter[k].Guid, strParameterCategory, MAX_CATEGORY_LENGTH);

      ValueTypeFromULONG(
         pEncoderParameters->Parameter[k].Type, strValueType, MAX_VALUE_TYPE_LENGTH);

      printf("    Parameter[%d]\n", k);
      wprintf(L"      The category is %s.\n", strParameterCategory);
      wprintf(L"      The data type is %s.\n", strValueType);

      printf("      The number of values is %d.\n",
      pEncoderParameters->Parameter[k].NumberOfValues); 
   } // for

   free(pEncoderParameters);
} // ShowAllEncoderParameters


HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   if(guid == EncoderCompression)
      hr = StringCchCopyW(category, maxChars, L"Compression");
   else if(guid == EncoderColorDepth)
      hr = StringCchCopyW(category, maxChars, L"ColorDepth");
   else if(guid == EncoderScanMethod)
      hr = StringCchCopyW(category, maxChars, L"ScanMethod");
   else if(guid == EncoderVersion)
      hr = StringCchCopyW(category, maxChars, L"Version");
   else if(guid == EncoderRenderMethod)
      hr = StringCchCopyW(category, maxChars, L"RenderMethod");
   else if(guid == EncoderQuality)
      hr = StringCchCopyW(category, maxChars, L"Quality");
   else if(guid == EncoderTransformation)
      hr = StringCchCopyW(category, maxChars, L"Transformation");
   else if(guid == EncoderLuminanceTable)
      hr = StringCchCopyW(category, maxChars, L"LuminanceTable");
   else if(guid == EncoderChrominanceTable)
      hr = StringCchCopyW(category, maxChars, L"ChrominanceTable");
   else if(guid == EncoderSaveFlag)
      hr = StringCchCopyW(category, maxChars, L"SaveFlag");
   else
      hr = StringCchCopyW(category, maxChars, L"Unknown category");

   return hr;
} // EncoderParameterCategoryFromGUID


HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* valueTypes[] = {
      L"Nothing",                  // 0
      L"ValueTypeByte",            // 1
      L"ValueTypeASCII",           // 2
      L"ValueTypeShort",           // 3
      L"ValueTypeLong",            // 4
      L"ValueTypeRational",        // 5
      L"ValueTypeLongRange",       // 6
      L"ValueTypeUndefined",       // 7
      L"ValueTypeRationalRange"};  // 8

   hr = StringCchCopyW(strValueType, maxChars, valueTypes[index]);
   return hr;

} // ValueTypeFromULONG
```



Lorsque vous exécutez l’application console précédente, vous recevez une sortie similaire à ce qui suit :


```
image/bmp
  The parameter list requires 0 bytes.

image/jpeg
  The parameter list requires 172 bytes.
  There are 4 EncoderParameter objects in the array.
    Parameter[0]
      The category is Transformation.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is Quality.
      The data type is LongRange.
      The number of values is 1.
    Parameter[2]
      The category is LuminanceTable.
      The data type is Short.
      The number of values is 0.
    Parameter[3]
      The category is ChrominanceTable.
      The data type is Short.
      The number of values is 0.

image/gif
  The parameter list requires 0 bytes.

image/tiff
  The parameter list requires 160 bytes.
  There are 3 EncoderParameter objects in the array.
    Parameter[0]
      The category is Compression.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is ColorDepth.
      The data type is Long.
      The number of values is 5.
    Parameter[2]
      The category is SaveFlag.
      The data type is Long.
      The number of values is 1.

image/png
  The parameter list requires 0 bytes.
```



Vous pouvez tirer les conclusions suivantes en examinant la sortie du programme précédent :

-   L’encodeur JPEG prend en charge les catégories de paramètres transformation, qualité, LuminanceTable et ChrominanceTable.
-   L’encodeur TIFF prend en charge les catégories de paramètres compression, ColorDepth et SaveFlag.

Vous pouvez également voir le nombre de valeurs acceptables pour chaque catégorie de paramètres. Par exemple, vous pouvez voir que la catégorie de paramètres ColorDepth (codec TIFF) a cinq valeurs de type **ULong**. Le code suivant répertorie ces cinq valeurs. Supposons que **pEncoderParameters** est un pointeur vers un objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) qui représente l’encodeur TIFF.


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[1].Value);
ULONG numVals = pEncoderParameters->Parameter[1].NumberOfValues;
printf("\nThe allowable values for ColorDepth are\n");

for(ULONG k = 0; k < numVals; ++k)
{
   printf("  %u\n", pUlong[k]);
}
            
```



Le code ci-dessus génère la sortie suivante :


```
The allowable values for ColorDepth are
  1
  4
  8
  24
  32
            
```



> [!Note]  
> Dans certains cas, les valeurs d’un objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) sont les valeurs numériques des éléments de l’énumération [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . Toutefois, les nombres de la liste précédente ne sont pas liés à l’énumération **EncoderValue** . Les nombres représentent 1 bit par pixel, 2 bits par pixel, et ainsi de suite.

 

Si vous écrivez du code semblable à l’exemple précédent pour étudier les valeurs autorisées pour les autres catégories de paramètres, vous obtiendrez un résultat similaire à ce qui suit.



| Paramètre d’encodeur JPEG | Valeurs autorisées                                                                                                                                                                                                 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transformation         | EncoderValueTransformRotate90 EncoderValueTransformRotate180<br/>  EncoderValueTransformRotate270<br/>  EncoderValueTransformFlipHorizontal<br/>  EncoderValueTransformFlipVertical<br/> |
| Qualité                | 0 à 100                                                                                                                                                                                                    |



 



| Paramètre d’encodeur TIFF | Valeurs autorisées                                                                                                                                                                             |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compression            | EncoderValueCompressionLZW EncoderValueCompressionCCITT3<br/>  EncoderValueCompressionCCITT4<br/>  EncoderValueCompressionRle<br/>  EncoderValueCompressionNone<br/> |
| La             | 1, 4, 8, 24, 32                                                                                                                                                                              |
| SaveFlag               | EncoderValueMultiFrame                                                                                                                                                                       |



 

> [!Note]  
> Si la largeur et la hauteur d’une image JPEG sont des multiples de 16, vous pouvez appliquer l’une des transformations autorisées par la catégorie de paramètre EncoderTransformation (par exemple, une rotation de 90 degrés) sans perte d’informations.

 

 

 
