---
title: MENUHEADER, structure
description: Contient des informations de version pour la ressource de menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menus de la structure MENUHEADER et autres ressources
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518060"
---
# <a name="menuheader-structure"></a><span data-ttu-id="de5fb-105">MENUHEADER, structure</span><span class="sxs-lookup"><span data-stu-id="de5fb-105">MENUHEADER structure</span></span>

<span data-ttu-id="de5fb-106">Contient des informations de version pour la ressource de menu.</span><span class="sxs-lookup"><span data-stu-id="de5fb-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="de5fb-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="de5fb-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de5fb-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="de5fb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="de5fb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="de5fb-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="de5fb-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="de5fb-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="de5fb-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="de5fb-112">Numéro de version du modèle de menu.</span><span class="sxs-lookup"><span data-stu-id="de5fb-112">The version number of the menu template.</span></span> <span data-ttu-id="de5fb-113">Ce membre doit être égal à zéro pour indiquer qu’il s’agit d’un [**\_ menu RT**](/windows/desktop/menurc/resource-types) créé avec un modèle de menu standard.</span><span class="sxs-lookup"><span data-stu-id="de5fb-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="de5fb-114">**cbHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="de5fb-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="de5fb-115">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="de5fb-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="de5fb-116">Taille de l’en-tête du modèle de menu.</span><span class="sxs-lookup"><span data-stu-id="de5fb-116">The size of the menu template header.</span></span> <span data-ttu-id="de5fb-117">Cette valeur est égale à zéro pour les menus que vous créez avec un modèle de menu standard.</span><span class="sxs-lookup"><span data-stu-id="de5fb-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de5fb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de5fb-118">Requirements</span></span>



| <span data-ttu-id="de5fb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de5fb-119">Requirement</span></span> | <span data-ttu-id="de5fb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="de5fb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="de5fb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de5fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de5fb-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de5fb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="de5fb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de5fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de5fb-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de5fb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="de5fb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de5fb-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="de5fb-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="de5fb-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="de5fb-127">**\_ \_ en-tête de modèle menuex**</span><span class="sxs-lookup"><span data-stu-id="de5fb-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="de5fb-128">**\_élément de modèle menuex \_**</span><span class="sxs-lookup"><span data-stu-id="de5fb-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="de5fb-129">**MENUITEMTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="de5fb-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="de5fb-130">**MENUITEMTEMPLATEHEADER**</span><span class="sxs-lookup"><span data-stu-id="de5fb-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="de5fb-131">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="de5fb-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="de5fb-132">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="de5fb-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="de5fb-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="de5fb-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de5fb-134">Ressources</span><span class="sxs-lookup"><span data-stu-id="de5fb-134">Resources</span></span>](resources.md)
</dt> </dl>

 

