---
title: Message TB_DELETEBUTTON (commctrl. h)
description: Supprime un bouton de la barre d’outils.
ms.assetid: 6ba569f0-c400-4c0d-bc9f-3a82bcef0360
keywords:
- TB_DELETEBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_DELETEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d9bbbca143351f70005990b5ac97fa4fa35cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942911"
---
# <a name="tb_deletebutton-message"></a><span data-ttu-id="c50b0-104">TO \_ DELETEBUTTON message</span><span class="sxs-lookup"><span data-stu-id="c50b0-104">TB\_DELETEBUTTON message</span></span>

<span data-ttu-id="c50b0-105">Supprime un bouton de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="c50b0-105">Deletes a button from the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c50b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c50b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c50b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c50b0-108">Index de base zéro du bouton à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c50b0-108">Zero-based index of the button to delete.</span></span>

</dd> <dt>

<span data-ttu-id="c50b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c50b0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c50b0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c50b0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50b0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c50b0-111">Return value</span></span>

<span data-ttu-id="c50b0-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c50b0-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c50b0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c50b0-113">Requirements</span></span>



| <span data-ttu-id="c50b0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c50b0-114">Requirement</span></span> | <span data-ttu-id="c50b0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c50b0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c50b0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c50b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c50b0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c50b0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c50b0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c50b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c50b0-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c50b0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c50b0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c50b0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50b0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50b0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





