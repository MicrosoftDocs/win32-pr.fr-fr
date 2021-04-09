---
title: Message TB_GETSTATE (commctrl. h)
description: Récupère des informations sur l’état du bouton spécifié dans une barre d’outils, par exemple s’il est activé, appuyé ou activé.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843246"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="1cd6e-104">TO \_ GETSTATE message</span><span class="sxs-lookup"><span data-stu-id="1cd6e-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="1cd6e-105">Récupère des informations sur l’état du bouton spécifié dans une barre d’outils, par exemple s’il est activé, appuyé ou activé.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cd6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cd6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd6e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cd6e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd6e-108">Identificateur de commande du bouton pour lequel des informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="1cd6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cd6e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1cd6e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd6e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cd6e-111">Return value</span></span>

<span data-ttu-id="1cd6e-112">Retourne les informations d’État du bouton en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="1cd6e-113">Les informations d’État du bouton peuvent être une combinaison des valeurs figurant dans États des boutons de la [**barre d’outils**](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="1cd6e-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd6e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cd6e-114">Requirements</span></span>



| <span data-ttu-id="1cd6e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cd6e-115">Requirement</span></span> | <span data-ttu-id="1cd6e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cd6e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd6e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cd6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd6e-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cd6e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cd6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd6e-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cd6e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cd6e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cd6e-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





