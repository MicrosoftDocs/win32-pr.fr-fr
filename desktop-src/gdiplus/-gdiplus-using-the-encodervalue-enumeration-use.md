---
description: Un encodeur donné prend en charge certaines catégories de paramètres, et pour chacune de ces catégories, cet encodeur autorise certaines valeurs.
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: Utilisation de l’énumération EncoderValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755248150e81f963ea1c5c597ab04649c342944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972823"
---
# <a name="using-the-encodervalue-enumeration"></a><span data-ttu-id="f30cf-103">Utilisation de l’énumération EncoderValue</span><span class="sxs-lookup"><span data-stu-id="f30cf-103">Using the EncoderValue Enumeration</span></span>

<span data-ttu-id="f30cf-104">Un encodeur donné prend en charge certaines catégories de paramètres, et pour chacune de ces catégories, cet encodeur autorise certaines valeurs.</span><span class="sxs-lookup"><span data-stu-id="f30cf-104">A given encoder supports certain parameter categories, and for each of those categories, that encoder allows certain values.</span></span> <span data-ttu-id="f30cf-105">Par exemple, l’encodeur JPEG prend en charge la catégorie de paramètre EncoderValueQuality, et les valeurs de paramètre autorisées sont les entiers de 0 à 100.</span><span class="sxs-lookup"><span data-stu-id="f30cf-105">For example, the JPEG encoder supports the EncoderValueQuality parameter category, and the allowable parameter values are the integers 0 through 100.</span></span> <span data-ttu-id="f30cf-106">Certaines des valeurs de paramètre autorisées sont les mêmes sur plusieurs encodeurs.</span><span class="sxs-lookup"><span data-stu-id="f30cf-106">Some of the allowable parameter values are the same across several encoders.</span></span> <span data-ttu-id="f30cf-107">Ces valeurs standard sont définies dans l’énumération [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) dans Gdiplusenums. h :</span><span class="sxs-lookup"><span data-stu-id="f30cf-107">These standard values are defined in the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration in Gdiplusenums.h:</span></span>


```
enum EncoderValue
{
   EncoderValueColorTypeCMYK,             // 0
   EncoderValueColorTypeYCCK,             // 1
   EncoderValueCompressionLZW,            // 2
   EncoderValueCompressionCCITT3,         // 3
   EncoderValueCompressionCCITT4,         // 4
   EncoderValueCompressionRle,            // 5
   EncoderValueCompressionNone,           // 6
   EncoderValueScanMethodInterlaced,      // 7
   EncoderValueScanMethodNonInterlaced,   // 8
   EncoderValueVersionGif87,              // 9
   EncoderValueVersionGif89,              // 10
   EncoderValueRenderProgressive,         // 11
   EncoderValueRenderNonProgressive,      // 12
   EncoderValueTransformRotate90,         // 13
   EncoderValueTransformRotate180,        // 14
   EncoderValueTransformRotate270,        // 15
   EncoderValueTransformFlipHorizontal,   // 16
   EncoderValueTransformFlipVertical,     // 17
   EncoderValueMultiFrame,                // 18
   EncoderValueLastFrame,                 // 19
   EncoderValueFlush,                     // 20
   EncoderValueFrameDimensionTime,        // 21
   EncoderValueFrameDimensionResolution,  // 22
   EncoderValueFrameDimensionPage         // 23
};
```



<span data-ttu-id="f30cf-108">L’une des catégories de paramètres prises en charge par l’encodeur JPEG est la catégorie EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="f30cf-108">One of the parameter categories supported by the JPEG encoder is the EncoderTransformation category.</span></span> <span data-ttu-id="f30cf-109">En examinant l’énumération [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) , vous pouvez spéculer (et être correct) que la catégorie EncoderTransformation autorise les cinq valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f30cf-109">By examining the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration, you might speculate (and you would be correct) that the EncoderTransformation category allows the following five values:</span></span>


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



<span data-ttu-id="f30cf-110">L’application console suivante vérifie que l’encodeur JPEG prend en charge la catégorie de paramètres EncoderTransformation et qu’il y a cinq valeurs autorisées pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f30cf-110">The following console application verifies that the JPEG encoder supports the EncoderTransformation parameter category and that there are five allowable values for such a parameter.</span></span> <span data-ttu-id="f30cf-111">La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="f30cf-111">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);
INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   // Create a Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);
   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);
   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);
   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);
   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);
   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);
   // Look at the first (index 0) EncoderParameter object in the array.
   printf("Parameter[0]\n");
   WCHAR strGuid[39];
   StringFromGUID2(pEncoderParameters->Parameter[0].Guid, strGuid, 39);
   wprintf(L"   The guid is %s.\n", strGuid);
   printf("   The data type is %d.\n", 
      pEncoderParameters->Parameter[0].Type);
   printf("   The number of values is %d.\n",
      pEncoderParameters->Parameter[0].NumberOfValues);
   free(pEncoderParameters);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="f30cf-112">Lorsque vous exécutez l’application console précédente, vous recevez une sortie similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="f30cf-112">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



<span data-ttu-id="f30cf-113">Vous pouvez rechercher le GUID dans Gdiplusimaging. h et savoir que la catégorie de cet objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="f30cf-113">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderTransformation.</span></span> <span data-ttu-id="f30cf-114">Dans Gdiplusenums. h, l’énumération [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indique que le type de données 4 est ValueLong (entier non signé 32 bits).</span><span class="sxs-lookup"><span data-stu-id="f30cf-114">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 4 is ValueLong (32-bit unsigned integer).</span></span> <span data-ttu-id="f30cf-115">Le nombre de valeurs étant de cinq, nous savons que le membre **value** de l’objet **EncoderParameter** est un pointeur vers un tableau de cinq valeurs **ULong** .</span><span class="sxs-lookup"><span data-stu-id="f30cf-115">The number of values is five, so we know that the **Value** member of the **EncoderParameter** object is a pointer to an array of five **ULONG** values.</span></span>

<span data-ttu-id="f30cf-116">Le code suivant est une suite de l’application console qui est présentée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="f30cf-116">The following code is a continuation of the console application that is shown in the preceding example.</span></span> <span data-ttu-id="f30cf-117">Le code répertorie les valeurs autorisées pour un paramètre EncoderTransformation :</span><span class="sxs-lookup"><span data-stu-id="f30cf-117">The code lists the allowable values for an EncoderTransformation parameter:</span></span>


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



<span data-ttu-id="f30cf-118">Le code ci-dessus génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="f30cf-118">The preceding code produces the following output:</span></span>


```
The allowable values are  13  14  15  16  17
```



<span data-ttu-id="f30cf-119">Les valeurs autorisées (13, 14, 15, 16 et 17) correspondent aux membres suivants de l’énumération [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="f30cf-119">The allowable values (13, 14, 15, 16, and 17) correspond to the following members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
