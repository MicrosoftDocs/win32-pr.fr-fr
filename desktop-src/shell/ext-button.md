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
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751013"
---
# <a name="ext_button-structure"></a><span data-ttu-id="78124-103">\_Structure du bouton ext</span><span class="sxs-lookup"><span data-stu-id="78124-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="78124-104">Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="78124-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="78124-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78124-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="78124-106">Membres</span><span class="sxs-lookup"><span data-stu-id="78124-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="78124-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="78124-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="78124-108">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="78124-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="78124-109">Identificateur de commande pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="78124-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="78124-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="78124-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="78124-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="78124-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="78124-112">Identificateur de la chaîne d’aide pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="78124-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="78124-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="78124-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="78124-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="78124-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="78124-115">Style du bouton.</span><span class="sxs-lookup"><span data-stu-id="78124-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78124-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="78124-116">Requirements</span></span>



| <span data-ttu-id="78124-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78124-117">Requirement</span></span> | <span data-ttu-id="78124-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="78124-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78124-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78124-119">Minimum supported client</span></span><br/> | <span data-ttu-id="78124-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78124-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="78124-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78124-121">Minimum supported server</span></span><br/> | <span data-ttu-id="78124-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78124-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="78124-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="78124-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="78124-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="78124-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78124-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78124-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78124-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="78124-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="78124-127">**\_TOOLBARLOAD FMS**</span><span class="sxs-lookup"><span data-stu-id="78124-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




