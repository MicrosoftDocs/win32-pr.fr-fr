---
description: Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.
title: Méthode ShellFolderView. PopupItemMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209940"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="e1132-103">Méthode ShellFolderView. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="e1132-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="e1132-104">Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1132-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1132-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1132-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="e1132-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1132-107">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1132-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1132-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e1132-108">Type: **Variant**</span></span>

<span data-ttu-id="e1132-109">Objet [**FolderItem**](folderitem.md) pour lequel le menu contextuel sera créé.</span><span class="sxs-lookup"><span data-stu-id="e1132-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="e1132-110">*VX* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e1132-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1132-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e1132-111">Type: **Variant**</span></span>

<span data-ttu-id="e1132-112">Position horizontale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="e1132-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e1132-113">*Vy* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e1132-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1132-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e1132-114">Type: **Variant**</span></span>

<span data-ttu-id="e1132-115">Position verticale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="e1132-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1132-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1132-116">Return value</span></span>

<span data-ttu-id="e1132-117">Type : \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="e1132-117">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="e1132-118">_ *String*\* qui reçoit la chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="e1132-118">The _ *String*\* that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1132-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e1132-119">Requirements</span></span>



| <span data-ttu-id="e1132-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1132-120">Requirement</span></span> | <span data-ttu-id="e1132-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1132-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1132-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1132-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1132-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1132-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e1132-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1132-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1132-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1132-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e1132-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1132-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1132-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1132-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e1132-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="e1132-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1132-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1132-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e1132-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e1132-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1132-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e1132-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
