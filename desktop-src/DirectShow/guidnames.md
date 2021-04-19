---
description: GuidNames est un tableau global dans la bibliothèque de classes de base DirectShow qui contient des chaînes représentant les GUID définis dans UUID. h. Ce tableau est utile pour générer la sortie de débogage.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537982"
---
# <a name="guidnames"></a><span data-ttu-id="50857-104">GuidNames</span><span class="sxs-lookup"><span data-stu-id="50857-104">GuidNames</span></span>

<span data-ttu-id="50857-105">`GuidNames` est un tableau global dans la bibliothèque de classes de base DirectShow qui contient des chaînes représentant les GUID définis dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="50857-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="50857-106">Ce tableau est utile pour générer la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="50857-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="50857-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50857-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50857-108"><span id="guid"></span><span id="GUID"></span>*uniques*</span><span class="sxs-lookup"><span data-stu-id="50857-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="50857-109">Spécifie toute valeur GUID définie dans le fichier d’en-tête UUID. h.</span><span class="sxs-lookup"><span data-stu-id="50857-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50857-110">Notes</span><span class="sxs-lookup"><span data-stu-id="50857-110">Remarks</span></span>

<span data-ttu-id="50857-111">Utilisez ce tableau global pour sortir les constantes GUID en tant que chaînes.</span><span class="sxs-lookup"><span data-stu-id="50857-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="50857-112">Par exemple, le code suivant imprime la chaîne « MEDIATYPE \_ Video » sur la console :</span><span class="sxs-lookup"><span data-stu-id="50857-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="50857-113">Si le GUID n’est pas mis en correspondance, la chaîne « nom GUID inconnu » est retournée.</span><span class="sxs-lookup"><span data-stu-id="50857-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="50857-114">Tous les GUID DirectShow ne sont pas définis dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="50857-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="50857-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50857-115">Requirements</span></span>



| <span data-ttu-id="50857-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50857-116">Requirement</span></span> | <span data-ttu-id="50857-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="50857-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50857-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="50857-118">Header</span></span><br/>  | <dl> <span data-ttu-id="50857-119"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50857-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50857-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50857-120">Library</span></span><br/> | <dl> <span data-ttu-id="50857-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="50857-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50857-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50857-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50857-123">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="50857-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




