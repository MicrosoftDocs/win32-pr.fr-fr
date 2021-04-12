---
title: FONTGROUPHDR, structure
description: Contient les informations nécessaires à une application pour accéder à une police spécifique. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menus de la structure FONTGROUPHDR et autres ressources
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200572"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="d10f2-105">FONTGROUPHDR, structure</span><span class="sxs-lookup"><span data-stu-id="d10f2-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="d10f2-106">Contient les informations nécessaires à une application pour accéder à une police spécifique.</span><span class="sxs-lookup"><span data-stu-id="d10f2-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="d10f2-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="d10f2-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d10f2-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="d10f2-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d10f2-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="d10f2-110">**NumberOfFonts**</span><span class="sxs-lookup"><span data-stu-id="d10f2-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="d10f2-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="d10f2-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="d10f2-112">Nombre de polices individuelles associées à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="d10f2-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="d10f2-113">**DE**</span><span class="sxs-lookup"><span data-stu-id="d10f2-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="d10f2-114">Type : **[ **dilocataire**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="d10f2-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d10f2-115">Structure qui contient un identificateur ordinal unique pour chaque police de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d10f2-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="d10f2-116">Le **membre est** un espace réservé pour le tableau de longueur variable de structures de [**diloyer**](direntry.md) .</span><span class="sxs-lookup"><span data-stu-id="d10f2-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d10f2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d10f2-117">Remarks</span></span>

<span data-ttu-id="d10f2-118">La structure **FONTGROUPHDR** suit les données pour les polices individuelles dans le. Fichier res.</span><span class="sxs-lookup"><span data-stu-id="d10f2-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="d10f2-119">Le compilateur de ressources ajoute automatiquement la structure **FONTGROUPHDR** , généralement comme dernière entrée dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d10f2-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10f2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d10f2-120">Requirements</span></span>



| <span data-ttu-id="d10f2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d10f2-121">Requirement</span></span> | <span data-ttu-id="d10f2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d10f2-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d10f2-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d10f2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d10f2-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d10f2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d10f2-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d10f2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d10f2-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d10f2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d10f2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d10f2-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d10f2-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d10f2-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d10f2-129">**Dilocataire**</span><span class="sxs-lookup"><span data-stu-id="d10f2-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="d10f2-130">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="d10f2-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="d10f2-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d10f2-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d10f2-132">Ressources</span><span class="sxs-lookup"><span data-stu-id="d10f2-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 





