---
title: Message TB_ISBUTTONPRESSED (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est enfoncé.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103225"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="c6273-104">TO \_ ISBUTTONPRESSED message</span><span class="sxs-lookup"><span data-stu-id="c6273-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="c6273-105">Détermine si le bouton spécifié dans une barre d’outils est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c6273-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6273-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6273-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6273-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6273-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="c6273-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="c6273-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6273-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c6273-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c6273-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6273-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6273-111">Return value</span></span>

<span data-ttu-id="c6273-112">Retourne une valeur différente de zéro si le bouton est enfoncé, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c6273-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6273-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6273-113">Requirements</span></span>



| <span data-ttu-id="c6273-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6273-114">Requirement</span></span> | <span data-ttu-id="c6273-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6273-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6273-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6273-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6273-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6273-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6273-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6273-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6273-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6273-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6273-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6273-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6273-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6273-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





