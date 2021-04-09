---
description: Recherche la BALIse enfant suivante dans le parent spécifié et retourne le TAGID de l’enfant suivant.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861049"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="2df97-103">SdbGetNextChild fonction)</span><span class="sxs-lookup"><span data-stu-id="2df97-103">SdbGetNextChild function</span></span>

<span data-ttu-id="2df97-104">Recherche la BALIse enfant suivante dans le parent spécifié et retourne le **TagId** de l’enfant suivant.</span><span class="sxs-lookup"><span data-stu-id="2df97-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2df97-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="2df97-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2df97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df97-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2df97-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df97-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="2df97-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2df97-109">*tiParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2df97-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df97-110">**TagId** du début de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2df97-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="2df97-111">Ce paramètre peut être **TagId \_ racine** ou **\_ \_ liste de types de balises**.</span><span class="sxs-lookup"><span data-stu-id="2df97-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="2df97-112">*tiPrev* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2df97-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df97-113">**TagId** de l’enfant précédent.</span><span class="sxs-lookup"><span data-stu-id="2df97-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df97-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2df97-114">Return value</span></span>

<span data-ttu-id="2df97-115">**TagId** de l’enfant ou **TagId \_ null** si aucun enfant n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="2df97-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="2df97-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2df97-116">Remarks</span></span>

<span data-ttu-id="2df97-117">Avant d’appeler cette fonction, appelez la fonction [**SdbGetFirstChild**](sdbgetfirstchild.md) .</span><span class="sxs-lookup"><span data-stu-id="2df97-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df97-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2df97-118">Requirements</span></span>



| <span data-ttu-id="2df97-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2df97-119">Requirement</span></span> | <span data-ttu-id="2df97-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2df97-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2df97-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2df97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2df97-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2df97-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2df97-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2df97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2df97-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2df97-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2df97-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2df97-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2df97-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2df97-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2df97-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2df97-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df97-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="2df97-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="2df97-129">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="2df97-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="2df97-130">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="2df97-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




