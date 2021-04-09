---
title: Structure de dilocataire
description: Contient un ordinal unique qui identifie une police individuelle dans le groupe de ressources de police. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menus de la structure dilocataires et autres ressources
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742029"
---
# <a name="direntry-structure"></a><span data-ttu-id="a5201-105">Structure de dilocataire</span><span class="sxs-lookup"><span data-stu-id="a5201-105">DIRENTRY structure</span></span>

<span data-ttu-id="a5201-106">Contient un ordinal unique qui identifie une police individuelle dans le groupe de ressources de police.</span><span class="sxs-lookup"><span data-stu-id="a5201-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="a5201-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="a5201-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5201-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5201-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="a5201-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a5201-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5201-110">**fontOrdinal**</span><span class="sxs-lookup"><span data-stu-id="a5201-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="a5201-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="a5201-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a5201-112">Identificateur ordinal unique pour une police individuelle dans un groupe de ressources de police.</span><span class="sxs-lookup"><span data-stu-id="a5201-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5201-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a5201-113">Remarks</span></span>

<span data-ttu-id="a5201-114">La structure [**FONTDIRENTRY**](fontdirentry.md) pour la police spécifiée suit directement la structure de **dilocataires** pour cette police.</span><span class="sxs-lookup"><span data-stu-id="a5201-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5201-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5201-115">Requirements</span></span>



| <span data-ttu-id="a5201-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5201-116">Requirement</span></span> | <span data-ttu-id="a5201-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5201-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a5201-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5201-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5201-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5201-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a5201-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5201-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5201-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5201-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a5201-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5201-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5201-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a5201-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a5201-124">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="a5201-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="a5201-125">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="a5201-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="a5201-126">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a5201-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a5201-127">Ressources</span><span class="sxs-lookup"><span data-stu-id="a5201-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





