---
description: La fonction PdhVbGetCounterPathFromList copie le chemin d’accès du compteur référencé par le paramètre d’index à partir d’une liste de chemins de compteurs créée par l’utilisateur à partir de l’appel le plus récent à la fonction PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529835"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="4d93e-103">PdhVbGetCounterPathFromList fonction)</span><span class="sxs-lookup"><span data-stu-id="4d93e-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="4d93e-104">La fonction **PdhVbGetCounterPathFromList** copie le chemin d’accès du compteur référencé par le paramètre d' *index* à partir d’une liste de chemins de compteurs créée par l’utilisateur à partir de l’appel le plus récent à la fonction [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="4d93e-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d93e-105">La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="4d93e-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="4d93e-106">Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4d93e-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="4d93e-107">Function PdhVbGetCounterPathFromList ( \_ index ByVal comme long, \_ ByVal buffer sous forme de chaîne, \_ ByVal BufferLength As long \_ ) As long</span><span class="sxs-lookup"><span data-stu-id="4d93e-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="4d93e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d93e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d93e-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="4d93e-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4d93e-110">Index du chemin d’accès du compteur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="4d93e-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="4d93e-111">Il doit s’agir d’une valeur supérieure ou égale à 1 et inférieure ou égale à la valeur retournée par la fonction [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .</span><span class="sxs-lookup"><span data-stu-id="4d93e-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4d93e-112">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="4d93e-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4d93e-113">Chaîne dimensionnée et initialisée qui recevra le chemin d’accès du compteur qui correspond à la valeur du paramètre d’index.</span><span class="sxs-lookup"><span data-stu-id="4d93e-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4d93e-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="4d93e-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="4d93e-115">Nombre maximal de caractères qui peuvent être contenus dans la chaîne référencée par la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4d93e-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d93e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d93e-116">Return value</span></span>

<span data-ttu-id="4d93e-117">La fonction retourne le nombre de caractères copiés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4d93e-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d93e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d93e-118">Requirements</span></span>



| <span data-ttu-id="4d93e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d93e-119">Requirement</span></span> | <span data-ttu-id="4d93e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d93e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d93e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d93e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4d93e-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d93e-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d93e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d93e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4d93e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d93e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4d93e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d93e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d93e-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d93e-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d93e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d93e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d93e-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d93e-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d93e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d93e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d93e-130">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="4d93e-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="4d93e-131">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="4d93e-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="4d93e-132">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="4d93e-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




