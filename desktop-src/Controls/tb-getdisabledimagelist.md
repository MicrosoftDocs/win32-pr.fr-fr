---
title: Message TB_GETDISABLEDIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- TB_GETDISABLEDIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942020"
---
# <a name="tb_getdisabledimagelist-message"></a><span data-ttu-id="6721e-104">TO \_ GETDISABLEDIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="6721e-104">TB\_GETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="6721e-105">Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons inactifs.</span><span class="sxs-lookup"><span data-stu-id="6721e-105">Retrieves the image list that a toolbar control uses to display inactive buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="6721e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6721e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6721e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6721e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6721e-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6721e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6721e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6721e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6721e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6721e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6721e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6721e-111">Return value</span></span>

<span data-ttu-id="6721e-112">Retourne le handle de la liste d’images inactives, ou **null** si aucune liste d’images inactives n’est définie.</span><span class="sxs-lookup"><span data-stu-id="6721e-112">Returns the handle to the inactive image list, or **NULL** if no inactive image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="6721e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6721e-113">Requirements</span></span>



| <span data-ttu-id="6721e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6721e-114">Requirement</span></span> | <span data-ttu-id="6721e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6721e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6721e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6721e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6721e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6721e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6721e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6721e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6721e-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6721e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6721e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6721e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6721e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6721e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





