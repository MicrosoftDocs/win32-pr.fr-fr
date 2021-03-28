---
description: 'La classe image fournit la méthode image :: GetEncoderParameterList afin que vous puissiez déterminer les paramètres qui sont pris en charge par un encodeur d’image donné.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Détermination des paramètres pris en charge par un encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991364"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="28bfb-103">Détermination des paramètres pris en charge par un encodeur</span><span class="sxs-lookup"><span data-stu-id="28bfb-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="28bfb-104">La classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fournit la méthode [**image :: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) afin que vous puissiez déterminer les paramètres qui sont pris en charge par un encodeur d’image donné.</span><span class="sxs-lookup"><span data-stu-id="28bfb-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="28bfb-105">La méthode **image :: GetEncoderParameterList** retourne un tableau d’objets [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="28bfb-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="28bfb-106">Vous devez allouer une mémoire tampon pour recevoir ce tableau avant d’appeler **image :: GetEncoderParameterList**.</span><span class="sxs-lookup"><span data-stu-id="28bfb-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="28bfb-107">Vous pouvez appeler [**image :: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) pour déterminer la taille de la mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="28bfb-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="28bfb-108">L’application console suivante obtient la liste des paramètres de l’encodeur JPEG.</span><span class="sxs-lookup"><span data-stu-id="28bfb-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="28bfb-109">La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="28bfb-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   // Create Bitmap (inherited from Image) object so that we can call
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

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="28bfb-110">Lorsque vous exécutez l’application console précédente, vous recevez une sortie similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="28bfb-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="28bfb-111">Chacun des objets [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) du tableau contient les quatre membres de données publics suivants :</span><span class="sxs-lookup"><span data-stu-id="28bfb-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="28bfb-112">Le code suivant est une suite de l’application console illustrée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="28bfb-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="28bfb-113">Le code examine le deuxième objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) dans le tableau retourné par [**image :: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span><span class="sxs-lookup"><span data-stu-id="28bfb-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="28bfb-114">Le code appelle [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), qui est une fonction système déclarée dans Objbase. h, pour convertir le membre **GUID** de l’objet **EncoderParameter** en chaîne.</span><span class="sxs-lookup"><span data-stu-id="28bfb-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



<span data-ttu-id="28bfb-115">Le code ci-dessus génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="28bfb-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="28bfb-116">Vous pouvez rechercher le GUID dans Gdiplusimaging. h et savoir que la catégorie de cet objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est EncoderQuality.</span><span class="sxs-lookup"><span data-stu-id="28bfb-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="28bfb-117">Vous pouvez utiliser cette catégorie (EncoderQuality) de paramètre pour définir le niveau de compression d’une image JPEG.</span><span class="sxs-lookup"><span data-stu-id="28bfb-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="28bfb-118">Dans Gdiplusenums. h, l’énumération [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indique que le type de données 6 est **ValueLongRange**.</span><span class="sxs-lookup"><span data-stu-id="28bfb-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="28bfb-119">Une plage longue est une paire de valeurs **ULong** .</span><span class="sxs-lookup"><span data-stu-id="28bfb-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="28bfb-120">Le nombre de valeurs étant un, nous savons que le membre **value** de l’objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est un pointeur vers un tableau qui possède un élément.</span><span class="sxs-lookup"><span data-stu-id="28bfb-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="28bfb-121">Qu’un élément est une paire de valeurs **ULong** .</span><span class="sxs-lookup"><span data-stu-id="28bfb-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="28bfb-122">Le code suivant est une suite de l’application console qui est présentée dans les deux exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="28bfb-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="28bfb-123">Le code définit un type de données appelé **PLONGRANGE** (pointeur vers une longue plage).</span><span class="sxs-lookup"><span data-stu-id="28bfb-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="28bfb-124">Une variable de type **PLONGRANGE** est utilisée pour extraire les valeurs minimales et maximales qui peuvent être transmises en tant que paramètre de qualité à l’encodeur JPEG.</span><span class="sxs-lookup"><span data-stu-id="28bfb-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



<span data-ttu-id="28bfb-125">Le code ci-dessus génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="28bfb-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="28bfb-126">Dans l’exemple précédent, la valeur retournée dans l’objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est une paire de valeurs **ULong** qui indiquent les valeurs minimales et maximales possibles pour le paramètre Quality.</span><span class="sxs-lookup"><span data-stu-id="28bfb-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="28bfb-127">Dans certains cas, les valeurs retournées dans un objet **EncoderParameter** sont des membres de l’énumération [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) .</span><span class="sxs-lookup"><span data-stu-id="28bfb-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="28bfb-128">Les rubriques suivantes décrivent l’énumération **EncoderValue** et les méthodes permettant de répertorier les valeurs de paramètres possibles plus en détail :</span><span class="sxs-lookup"><span data-stu-id="28bfb-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="28bfb-129">Utilisation de l’énumération EncoderValue</span><span class="sxs-lookup"><span data-stu-id="28bfb-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="28bfb-130">Liste des paramètres et des valeurs pour tous les encodeurs</span><span class="sxs-lookup"><span data-stu-id="28bfb-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
