---
title: MENUHELPID, structure
description: Contient les données finales écrites dans la \_ ressource de menu RT pour un menu ou un sous-menu si le membre resInfo de la structure POPUPMENUITEM est défini sur MFR \_ Popup.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menus de la structure MENUHELPID et autres ressources
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511594"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="72011-104">MENUHELPID, structure</span><span class="sxs-lookup"><span data-stu-id="72011-104">MENUHELPID structure</span></span>

<span data-ttu-id="72011-105">Contient les données finales écrites dans la ressource de [**\_ menu RT**](/windows/desktop/menurc/resource-types) pour un menu ou un sous-menu si le membre **ResInfo** de la structure [**POPUPMENUITEM**](popupmenuitem.md) est défini sur **MFR \_ Popup**.</span><span class="sxs-lookup"><span data-stu-id="72011-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="72011-106">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="72011-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="72011-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72011-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="72011-108">Membres</span><span class="sxs-lookup"><span data-stu-id="72011-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72011-109">**helpID**</span><span class="sxs-lookup"><span data-stu-id="72011-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="72011-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="72011-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="72011-111">Identificateur utilisé pour identifier le menu lors du traitement [**de \_ l’aide WM**](/windows/desktop/shell/wm-help) .</span><span class="sxs-lookup"><span data-stu-id="72011-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72011-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72011-112">Requirements</span></span>



| <span data-ttu-id="72011-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72011-113">Requirement</span></span> | <span data-ttu-id="72011-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="72011-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="72011-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72011-115">Minimum supported client</span></span><br/> | <span data-ttu-id="72011-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72011-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="72011-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72011-117">Minimum supported server</span></span><br/> | <span data-ttu-id="72011-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72011-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="72011-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72011-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="72011-120">**Référence**</span><span class="sxs-lookup"><span data-stu-id="72011-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="72011-121">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="72011-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="72011-122">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="72011-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="72011-123">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="72011-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="72011-124">Ressources</span><span class="sxs-lookup"><span data-stu-id="72011-124">Resources</span></span>](resources.md)
</dt> </dl>

 

