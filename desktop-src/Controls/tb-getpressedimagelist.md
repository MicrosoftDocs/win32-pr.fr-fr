---
title: Message TB_GETPRESSEDIMAGELIST (commctrl. h)
description: Obtient la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans un état appuyé.
ms.assetid: 116d4212-48ea-4b00-a752-21e5e1f10e36
keywords:
- TB_GETPRESSEDIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3028b119eb7f84a66caf0b6978382cee569b4a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106441"
---
# <a name="tb_getpressedimagelist-message"></a><span data-ttu-id="4397a-104">TO \_ GETPRESSEDIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="4397a-104">TB\_GETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="4397a-105">Obtient la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons dans un état appuyé.</span><span class="sxs-lookup"><span data-stu-id="4397a-105">Gets the image list that a toolbar control uses to display buttons in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="4397a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4397a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4397a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4397a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4397a-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4397a-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4397a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4397a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4397a-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4397a-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4397a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4397a-111">Return value</span></span>

<span data-ttu-id="4397a-112">Retourne le handle de la liste d’images, ou **null** si aucune liste d’images n’est définie.</span><span class="sxs-lookup"><span data-stu-id="4397a-112">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="4397a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4397a-113">Requirements</span></span>



| <span data-ttu-id="4397a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4397a-114">Requirement</span></span> | <span data-ttu-id="4397a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4397a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4397a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4397a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4397a-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4397a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4397a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4397a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4397a-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4397a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4397a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4397a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4397a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4397a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





