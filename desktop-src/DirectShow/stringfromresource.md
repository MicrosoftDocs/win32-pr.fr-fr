---
description: La fonction StringFromResource charge une chaîne à partir d’un fichier de ressources avec l’identificateur de ressource donné.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: StringFromResource, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545626"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="eb9c8-103">StringFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="eb9c8-103">StringFromResource function</span></span>

<span data-ttu-id="eb9c8-104">La `StringFromResource` fonction charge une chaîne à partir d’un fichier de ressources avec l’identificateur de ressource donné.</span><span class="sxs-lookup"><span data-stu-id="eb9c8-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb9c8-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="eb9c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb9c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9c8-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="eb9c8-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="eb9c8-108">Pointeur vers la chaîne correspondant à *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="eb9c8-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="eb9c8-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="eb9c8-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="eb9c8-110">Identificateur de ressource de la chaîne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="eb9c8-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9c8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb9c8-111">Return value</span></span>

<span data-ttu-id="eb9c8-112">Retourne la même chaîne que *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="eb9c8-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="eb9c8-113">Si la fonction échoue, retourne une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="eb9c8-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9c8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="eb9c8-114">Remarks</span></span>

<span data-ttu-id="eb9c8-115">La mémoire tampon *pbuffer* doit avoir au moins une \_ longueur maximale de Str \_ octets.</span><span class="sxs-lookup"><span data-stu-id="eb9c8-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9c8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb9c8-116">Requirements</span></span>



| <span data-ttu-id="eb9c8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb9c8-117">Requirement</span></span> | <span data-ttu-id="eb9c8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb9c8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9c8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb9c8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="eb9c8-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb9c8-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="eb9c8-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb9c8-121">Library</span></span><br/> | <dl> <span data-ttu-id="eb9c8-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eb9c8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb9c8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb9c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9c8-124">Fonctions d’assistance de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="eb9c8-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




