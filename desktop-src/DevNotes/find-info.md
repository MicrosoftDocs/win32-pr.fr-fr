---
description: Contient les informations de contexte de recherche.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Structure FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513304"
---
# <a name="find_info-structure"></a><span data-ttu-id="aa16e-103">Rechercher la \_ structure des informations</span><span class="sxs-lookup"><span data-stu-id="aa16e-103">FIND\_INFO structure</span></span>

<span data-ttu-id="aa16e-104">Contient les informations de contexte de recherche.</span><span class="sxs-lookup"><span data-stu-id="aa16e-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa16e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa16e-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="aa16e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="aa16e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa16e-107">**tiIndex**</span><span class="sxs-lookup"><span data-stu-id="aa16e-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-108">**TagId** de l’index dans lequel effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="aa16e-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-109">**tiCurrent**</span><span class="sxs-lookup"><span data-stu-id="aa16e-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-110">**TagId** pour l’élément actuel qui a été localisé.</span><span class="sxs-lookup"><span data-stu-id="aa16e-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-111">**tiEndIndex**</span><span class="sxs-lookup"><span data-stu-id="aa16e-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-112">**TagId** pour le dernier enregistrement après FindFirst si l’index est unique.</span><span class="sxs-lookup"><span data-stu-id="aa16e-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="aa16e-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-114">Type de l’élément à localiser.</span><span class="sxs-lookup"><span data-stu-id="aa16e-114">The type of the item to be located.</span></span> <span data-ttu-id="aa16e-115">Consultez [types de balises](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="aa16e-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-116">**dwIndexRec**</span><span class="sxs-lookup"><span data-stu-id="aa16e-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-117">Compteur interne utilisé pour effectuer le suivi de l’emplacement de début de l’opération de recherche suivante dans l’index.</span><span class="sxs-lookup"><span data-stu-id="aa16e-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="aa16e-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-119">Ce membre peut être 0 ou **SHIMDB \_ \_ \_ clé unique d’index** (0x00000001), qui indique qu’il s’agit d’un index de clé unique.</span><span class="sxs-lookup"><span data-stu-id="aa16e-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-120">**ullKey**</span><span class="sxs-lookup"><span data-stu-id="aa16e-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-121">Clé de l’entrée en cours.</span><span class="sxs-lookup"><span data-stu-id="aa16e-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="aa16e-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-123">Chaîne actuelle (si le type de balise est le **type de balise \_ \_ STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="aa16e-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-124">**dwName**</span><span class="sxs-lookup"><span data-stu-id="aa16e-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-125">Valeur **DWORD** actuelle (si le type de balise **est \_ \_ DWORD type de balise**).</span><span class="sxs-lookup"><span data-stu-id="aa16e-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="aa16e-126">**pguidName**</span><span class="sxs-lookup"><span data-stu-id="aa16e-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="aa16e-127">La valeur actuelle du GUID (si le type de balise est **\_ \_ Binary type de balise** et la balise est **tag \_ Database \_ ID**).</span><span class="sxs-lookup"><span data-stu-id="aa16e-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa16e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa16e-128">Requirements</span></span>



| <span data-ttu-id="aa16e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa16e-129">Requirement</span></span> | <span data-ttu-id="aa16e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa16e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa16e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa16e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="aa16e-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa16e-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa16e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa16e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="aa16e-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa16e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa16e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa16e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa16e-136">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="aa16e-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




