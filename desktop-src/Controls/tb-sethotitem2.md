---
title: Message TB_SETHOTITEM2 (commctrl. h)
description: Définit l’élément réactif dans une barre d’outils.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742652"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="b515a-104">TO \_ SETHOTITEM2 message</span><span class="sxs-lookup"><span data-stu-id="b515a-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="b515a-105">Définit l’élément réactif dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="b515a-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b515a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b515a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b515a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b515a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b515a-108">Index de l’élément qui sera rendu chaud.</span><span class="sxs-lookup"><span data-stu-id="b515a-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="b515a-109">Si cette valeur est-1, aucun des éléments n’est chaud.</span><span class="sxs-lookup"><span data-stu-id="b515a-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="b515a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b515a-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b515a-111">Combinaison d’indicateurs HICF \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="b515a-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="b515a-112">Consultez <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="b515a-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b515a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b515a-113">Return value</span></span>

<span data-ttu-id="b515a-114">Retourne l’index de l’élément réactif précédent, ou-1 s’il n’y a pas d’élément réactif.</span><span class="sxs-lookup"><span data-stu-id="b515a-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b515a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b515a-115">Remarks</span></span>

<span data-ttu-id="b515a-116">Le comportement de ce message n’est pas défini pour les barres d’outils qui n’ont pas le style [**\_ plat TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b515a-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b515a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b515a-117">Requirements</span></span>



| <span data-ttu-id="b515a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b515a-118">Requirement</span></span> | <span data-ttu-id="b515a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b515a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b515a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b515a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b515a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b515a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b515a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b515a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b515a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b515a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b515a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b515a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b515a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b515a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





