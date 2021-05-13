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
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842190"
---
# <a name="fms_load-structure"></a><span data-ttu-id="572b4-104">\_Structure de charge FMS</span><span class="sxs-lookup"><span data-stu-id="572b4-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="572b4-105">Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="572b4-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="572b4-106">La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="572b4-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="572b4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="572b4-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="572b4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="572b4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="572b4-109">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="572b4-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="572b4-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="572b4-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="572b4-111">Longueur, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="572b4-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="572b4-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="572b4-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="572b4-113">Type : **\[ \_ \_ longueur \] du texte du menu TCHAR**</span><span class="sxs-lookup"><span data-stu-id="572b4-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="572b4-114">Nom se terminant par un caractère NULL d’un élément de menu qui s’affiche dans la barre de menus du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="572b4-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="572b4-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="572b4-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="572b4-116">Type : **HMENU**</span><span class="sxs-lookup"><span data-stu-id="572b4-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="572b4-117">Identificateur du menu contextuel ajouté à la barre de menus dans le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="572b4-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="572b4-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="572b4-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="572b4-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="572b4-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="572b4-120">Valeur delta de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="572b4-120">The menu item delta value.</span></span> <span data-ttu-id="572b4-121">Pour éviter les conflits avec ses propres éléments de menu, le gestionnaire de fichiers renumérote les identificateurs d’élément de menu dans le menu contextuel identifié par le membre **HMENU** en ajoutant cette valeur Delta à chaque identificateur.</span><span class="sxs-lookup"><span data-stu-id="572b4-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="572b4-122">Une DLL d’extension qui doit modifier un élément de menu doit identifier l’élément en ajoutant la valeur Delta à l’identificateur de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="572b4-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="572b4-123">La valeur de ce membre peut varier de la session à la session.</span><span class="sxs-lookup"><span data-stu-id="572b4-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="572b4-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="572b4-124">Requirements</span></span>



| <span data-ttu-id="572b4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="572b4-125">Requirement</span></span> | <span data-ttu-id="572b4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="572b4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="572b4-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="572b4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="572b4-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="572b4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="572b4-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="572b4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="572b4-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="572b4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="572b4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="572b4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="572b4-132"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="572b4-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572b4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="572b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572b4-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="572b4-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




