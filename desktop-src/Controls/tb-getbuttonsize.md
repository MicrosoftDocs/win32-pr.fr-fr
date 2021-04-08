---
title: Message TB_GETBUTTONSIZE (commctrl. h)
description: Récupère la largeur et la hauteur actuelles des boutons de la barre d’outils, en pixels.
ms.assetid: c1b72494-670b-4cf8-a78f-c67b6eee0677
keywords:
- TB_GETBUTTONSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a414f5b338353d7d8ce22a081e9b711a2b56a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844446"
---
# <a name="tb_getbuttonsize-message"></a><span data-ttu-id="b0b85-104">TO \_ GETBUTTONSIZE message</span><span class="sxs-lookup"><span data-stu-id="b0b85-104">TB\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="b0b85-105">Récupère la largeur et la hauteur actuelles des boutons de la barre d’outils, en pixels.</span><span class="sxs-lookup"><span data-stu-id="b0b85-105">Retrieves the current width and height of toolbar buttons, in pixels.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0b85-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0b85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0b85-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b0b85-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b0b85-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b0b85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0b85-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b0b85-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b0b85-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b85-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0b85-111">Return value</span></span>

<span data-ttu-id="b0b85-112">Retourne une valeur **DWORD** qui contient les valeurs de largeur et de hauteur dans le mot de poids faible et le mot de poids fort, respectivement.</span><span class="sxs-lookup"><span data-stu-id="b0b85-112">Returns a **DWORD** value that contains the width and height values in the low word and high word, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b85-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0b85-113">Requirements</span></span>



| <span data-ttu-id="b0b85-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b85-114">Requirement</span></span> | <span data-ttu-id="b0b85-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b85-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b85-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0b85-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b85-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0b85-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0b85-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0b85-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b85-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0b85-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0b85-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0b85-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b85-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b85-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





