---
description: Contient des informations utilisées par le gestionnaire de fichiers pour ajouter une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.
title: Structure FMS_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842210"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="507ea-103">Structure de FMS \_ HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="507ea-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="507ea-104">Contient des informations utilisées par le gestionnaire de fichiers pour ajouter une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="507ea-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="507ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="507ea-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="507ea-106">Membres</span><span class="sxs-lookup"><span data-stu-id="507ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="507ea-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="507ea-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="507ea-108">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="507ea-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="507ea-109">Identificateur de l’élément de commande.</span><span class="sxs-lookup"><span data-stu-id="507ea-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="507ea-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="507ea-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="507ea-111">Type : **HMENU**</span><span class="sxs-lookup"><span data-stu-id="507ea-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="507ea-112">Identificateur de la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="507ea-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="507ea-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="507ea-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="507ea-114">Type : **\_ \_ WCHAR \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="507ea-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="507ea-115">Chaîne terminée par le caractère null qui reçoit le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="507ea-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="507ea-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="507ea-116">Requirements</span></span>



| <span data-ttu-id="507ea-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="507ea-117">Requirement</span></span> | <span data-ttu-id="507ea-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="507ea-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="507ea-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="507ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="507ea-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="507ea-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="507ea-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="507ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="507ea-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="507ea-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="507ea-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="507ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="507ea-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="507ea-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507ea-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="507ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507ea-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="507ea-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="507ea-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="507ea-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




