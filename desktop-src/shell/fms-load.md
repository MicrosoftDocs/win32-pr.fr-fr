---
description: Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers. La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.
title: Structure FMS_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971915"
---
# <a name="fms_load-structure"></a><span data-ttu-id="33bbf-104">\_Structure de charge FMS</span><span class="sxs-lookup"><span data-stu-id="33bbf-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="33bbf-105">Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33bbf-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="33bbf-106">La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33bbf-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="33bbf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33bbf-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="33bbf-108">Membres</span><span class="sxs-lookup"><span data-stu-id="33bbf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="33bbf-109">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="33bbf-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="33bbf-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="33bbf-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="33bbf-111">Longueur, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="33bbf-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="33bbf-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="33bbf-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="33bbf-113">Type : **\[ \_ \_ longueur \] du texte du menu TCHAR**</span><span class="sxs-lookup"><span data-stu-id="33bbf-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="33bbf-114">Nom se terminant par un caractère NULL d’un élément de menu qui s’affiche dans la barre de menus du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33bbf-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="33bbf-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="33bbf-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="33bbf-116">Type : **HMENU**</span><span class="sxs-lookup"><span data-stu-id="33bbf-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="33bbf-117">Identificateur du menu contextuel ajouté à la barre de menus dans le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33bbf-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="33bbf-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="33bbf-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="33bbf-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="33bbf-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="33bbf-120">Valeur delta de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="33bbf-120">The menu item delta value.</span></span> <span data-ttu-id="33bbf-121">Pour éviter les conflits avec ses propres éléments de menu, le gestionnaire de fichiers renumérote les identificateurs d’élément de menu dans le menu contextuel identifié par le membre **HMENU** en ajoutant cette valeur Delta à chaque identificateur.</span><span class="sxs-lookup"><span data-stu-id="33bbf-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="33bbf-122">Une DLL d’extension qui doit modifier un élément de menu doit identifier l’élément en ajoutant la valeur Delta à l’identificateur de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="33bbf-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="33bbf-123">La valeur de ce membre peut varier de la session à la session.</span><span class="sxs-lookup"><span data-stu-id="33bbf-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33bbf-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="33bbf-124">Requirements</span></span>



| <span data-ttu-id="33bbf-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33bbf-125">Requirement</span></span> | <span data-ttu-id="33bbf-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="33bbf-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33bbf-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33bbf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="33bbf-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33bbf-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="33bbf-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33bbf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="33bbf-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33bbf-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="33bbf-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="33bbf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="33bbf-132"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="33bbf-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bbf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33bbf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bbf-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="33bbf-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




