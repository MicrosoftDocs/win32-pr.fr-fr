---
description: 'La classe image fournit la méthode image :: GetEncoderParameterList afin que vous puissiez déterminer les paramètres qui sont pris en charge par un encodeur d’image donné.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Détermination des paramètres pris en charge par un encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c842b14a2d14af578eede428e79018a2d266ea6133ed61a9bd0736e8dadc97e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977569"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Détermination des paramètres pris en charge par un encodeur

La classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fournit la méthode [**image :: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) afin que vous puissiez déterminer les paramètres qui sont pris en charge par un encodeur d’image donné. La méthode **image :: GetEncoderParameterList** retourne un tableau d’objets [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Vous devez allouer une mémoire tampon pour recevoir ce tableau avant d’appeler **image :: GetEncoderParameterList**. Vous pouvez appeler [**image :: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) pour déterminer la taille de la mémoire tampon requise.

L’application console suivante obtient la liste des paramètres de l’encodeur JPEG. La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



Lorsque vous exécutez l’application console précédente, vous recevez une sortie similaire à ce qui suit :


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Chacun des objets [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) du tableau contient les quatre membres de données publics suivants :

Le code suivant est une suite de l’application console illustrée dans l’exemple précédent. Le code examine le deuxième objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) dans le tableau retourné par [**image :: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist). Le code appelle [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), qui est une fonction système déclarée dans Objbase. h, pour convertir le membre **GUID** de l’objet **EncoderParameter** en chaîne.


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



Le code ci-dessus génère la sortie suivante :


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



Vous pouvez rechercher le GUID dans Gdiplusimaging. h et savoir que la catégorie de cet objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est EncoderQuality. Vous pouvez utiliser cette catégorie (EncoderQuality) de paramètre pour définir le niveau de compression d’une image JPEG.

Dans Gdiplusenums. h, l’énumération [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indique que le type de données 6 est **ValueLongRange**. Une plage longue est une paire de valeurs **ULong** .

Le nombre de valeurs étant un, nous savons que le membre **value** de l’objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est un pointeur vers un tableau qui possède un élément. Qu’un élément est une paire de valeurs **ULong** .

Le code suivant est une suite de l’application console qui est présentée dans les deux exemples précédents. Le code définit un type de données appelé **PLONGRANGE** (pointeur vers une longue plage). Une variable de type **PLONGRANGE** est utilisée pour extraire les valeurs minimales et maximales qui peuvent être transmises en tant que paramètre de qualité à l’encodeur JPEG.


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



Le code ci-dessus génère la sortie suivante :


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



Dans l’exemple précédent, la valeur retournée dans l’objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) est une paire de valeurs **ULong** qui indiquent les valeurs minimales et maximales possibles pour le paramètre Quality. Dans certains cas, les valeurs retournées dans un objet **EncoderParameter** sont des membres de l’énumération [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . Les rubriques suivantes décrivent l’énumération **EncoderValue** et les méthodes permettant de répertorier les valeurs de paramètres possibles plus en détail :

-   [Utilisation de l’énumération EncoderValue](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Liste des paramètres et des valeurs pour tous les encodeurs](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
