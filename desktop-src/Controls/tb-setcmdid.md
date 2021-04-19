---
title: Message TB_SETCMDID (commctrl. h)
description: Définit l’identificateur de commande d’un bouton de barre d’outils.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- TB_SETCMDID les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509719"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="57e1c-104">TO \_ SETCMDID message</span><span class="sxs-lookup"><span data-stu-id="57e1c-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="57e1c-105">Définit l’identificateur de commande d’un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="57e1c-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="57e1c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e1c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57e1c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57e1c-108">Index de base zéro du bouton dont l’identificateur de commande doit être défini.</span><span class="sxs-lookup"><span data-stu-id="57e1c-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="57e1c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57e1c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57e1c-110">Identificateur de commande.</span><span class="sxs-lookup"><span data-stu-id="57e1c-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57e1c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57e1c-111">Return value</span></span>

<span data-ttu-id="57e1c-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="57e1c-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e1c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57e1c-113">Requirements</span></span>



| <span data-ttu-id="57e1c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57e1c-114">Requirement</span></span> | <span data-ttu-id="57e1c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="57e1c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57e1c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57e1c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="57e1c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57e1c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57e1c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57e1c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="57e1c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57e1c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57e1c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="57e1c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="57e1c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57e1c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





