---
title: Message TB_SETHOTITEM (commctrl. h)
description: 'TB_SETHOTITEM message : définit l’élément réactif dans une barre d’outils.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104177"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="3c0ec-104">TO \_ SETHOTITEM message</span><span class="sxs-lookup"><span data-stu-id="3c0ec-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="3c0ec-105">Définit l’élément réactif dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c0ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c0ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c0ec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0ec-108">Index de l’élément qui sera rendu chaud.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="3c0ec-109">Si cette valeur est-1, aucun des éléments n’est chaud.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="3c0ec-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c0ec-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3c0ec-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0ec-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c0ec-112">Return value</span></span>

<span data-ttu-id="3c0ec-113">Retourne l’index de l’élément réactif précédent, ou-1 s’il n’y a pas d’élément réactif.</span><span class="sxs-lookup"><span data-stu-id="3c0ec-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c0ec-114">Notes </span><span class="sxs-lookup"><span data-stu-id="3c0ec-114">Remarks</span></span>

<span data-ttu-id="3c0ec-115">Le comportement de ce message n’est pas défini pour les barres d’outils qui n’ont pas le style [**\_ plat TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3c0ec-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0ec-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c0ec-116">Requirements</span></span>



| <span data-ttu-id="3c0ec-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c0ec-117">Requirement</span></span> | <span data-ttu-id="3c0ec-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c0ec-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0ec-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c0ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0ec-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c0ec-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c0ec-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c0ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0ec-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c0ec-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c0ec-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c0ec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0ec-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c0ec-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





