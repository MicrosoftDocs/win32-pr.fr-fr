---
description: La fonction WideStringFromResource charge une chaîne à caractères larges à partir d’un fichier de ressources avec l’identificateur de ressource donné.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: WideStringFromResource, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540520"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="2a72f-103">WideStringFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="2a72f-103">WideStringFromResource function</span></span>

<span data-ttu-id="2a72f-104">La `WideStringFromResource` fonction charge une chaîne de caractères larges à partir d’un fichier de ressources avec l’identificateur de ressource donné.</span><span class="sxs-lookup"><span data-stu-id="2a72f-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a72f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a72f-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="2a72f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a72f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a72f-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="2a72f-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="2a72f-108">Pointeur vers la chaîne correspondant à *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="2a72f-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="2a72f-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="2a72f-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="2a72f-110">Identificateur de ressource de la chaîne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2a72f-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a72f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a72f-111">Return value</span></span>

<span data-ttu-id="2a72f-112">Retourne la même chaîne que *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="2a72f-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="2a72f-113">Si la fonction échoue, retourne une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="2a72f-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a72f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2a72f-114">Remarks</span></span>

<span data-ttu-id="2a72f-115">Les pages de propriétés sont généralement appelées par le biais de leurs interfaces COM, qui utilisent des chaînes de caractères larges, quelle que soit la façon dont le binaire est généré.</span><span class="sxs-lookup"><span data-stu-id="2a72f-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="2a72f-116">Cette fonction vous permet de convertir une chaîne de ressource en une chaîne de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="2a72f-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="2a72f-117">La fonction convertit la ressource en une chaîne de caractères larges (si elle ne l’est pas déjà) après l’avoir chargée.</span><span class="sxs-lookup"><span data-stu-id="2a72f-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a72f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a72f-118">Requirements</span></span>



| <span data-ttu-id="2a72f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a72f-119">Requirement</span></span> | <span data-ttu-id="2a72f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a72f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a72f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a72f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2a72f-122"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a72f-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2a72f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a72f-123">Library</span></span><br/> | <dl> <span data-ttu-id="2a72f-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2a72f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a72f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a72f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a72f-126">Fonctions d’assistance de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="2a72f-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




