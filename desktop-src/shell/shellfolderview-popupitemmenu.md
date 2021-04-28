---
description: 'Méthode ShellFolderView. PopupItemMenu : crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.'
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
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083387"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="779cb-103">Méthode ShellFolderView. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="779cb-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="779cb-104">Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="779cb-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="779cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="779cb-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="779cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="779cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="779cb-107">*vItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="779cb-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="779cb-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="779cb-108">Type: **Variant**</span></span>

<span data-ttu-id="779cb-109">Objet [**FolderItem**](folderitem.md) pour lequel le menu contextuel sera créé.</span><span class="sxs-lookup"><span data-stu-id="779cb-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="779cb-110">*VX* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="779cb-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="779cb-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="779cb-111">Type: **Variant**</span></span>

<span data-ttu-id="779cb-112">Position horizontale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="779cb-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="779cb-113">*Vy* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="779cb-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="779cb-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="779cb-114">Type: **Variant**</span></span>

<span data-ttu-id="779cb-115">Position verticale du menu, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="779cb-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="779cb-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="779cb-116">Return value</span></span>

<span data-ttu-id="779cb-117">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="779cb-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="779cb-118">**Chaîne** qui reçoit la chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="779cb-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="779cb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="779cb-119">Requirements</span></span>



| <span data-ttu-id="779cb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="779cb-120">Requirement</span></span> | <span data-ttu-id="779cb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="779cb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779cb-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="779cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="779cb-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="779cb-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="779cb-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="779cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="779cb-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="779cb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="779cb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="779cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="779cb-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="779cb-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="779cb-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="779cb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="779cb-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="779cb-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="779cb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="779cb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="779cb-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="779cb-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
