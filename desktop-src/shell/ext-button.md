---
description: Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.
title: Structure EXT_BUTTON (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843150"
---
# <a name="ext_button-structure"></a><span data-ttu-id="670b7-103">\_Structure du bouton ext</span><span class="sxs-lookup"><span data-stu-id="670b7-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="670b7-104">Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="670b7-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="670b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="670b7-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="670b7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="670b7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="670b7-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="670b7-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="670b7-108">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="670b7-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="670b7-109">Identificateur de commande pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="670b7-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="670b7-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="670b7-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="670b7-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="670b7-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="670b7-112">Identificateur de la chaîne d’aide pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="670b7-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="670b7-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="670b7-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="670b7-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="670b7-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="670b7-115">Style du bouton.</span><span class="sxs-lookup"><span data-stu-id="670b7-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="670b7-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="670b7-116">Requirements</span></span>



| <span data-ttu-id="670b7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="670b7-117">Requirement</span></span> | <span data-ttu-id="670b7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="670b7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="670b7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670b7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="670b7-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="670b7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="670b7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670b7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="670b7-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="670b7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="670b7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="670b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="670b7-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="670b7-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670b7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="670b7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670b7-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="670b7-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="670b7-127">**\_TOOLBARLOAD FMS**</span><span class="sxs-lookup"><span data-stu-id="670b7-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




