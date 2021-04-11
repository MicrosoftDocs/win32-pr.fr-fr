---
title: Message EM_GETOPTIONS (RichEdit. h)
description: Récupère les options de contrôle RichEdit.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942481"
---
# <a name="em_getoptions-message"></a><span data-ttu-id="ae76f-104">Message des préversions EM \_</span><span class="sxs-lookup"><span data-stu-id="ae76f-104">EM\_GETOPTIONS message</span></span>

<span data-ttu-id="ae76f-105">Récupère les options de contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="ae76f-105">Retrieves rich edit control options.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae76f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae76f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae76f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae76f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae76f-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae76f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ae76f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae76f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae76f-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae76f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae76f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae76f-111">Return value</span></span>

<span data-ttu-id="ae76f-112">Ce message retourne une combinaison des valeurs d’indicateur d’option actuelles décrites dans le message [**em \_ SETOPTIONS**](em-setoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="ae76f-112">This message returns a combination of the current option flag values described in the [**EM\_SETOPTIONS**](em-setoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae76f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae76f-113">Requirements</span></span>



| <span data-ttu-id="ae76f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae76f-114">Requirement</span></span> | <span data-ttu-id="ae76f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae76f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae76f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae76f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ae76f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae76f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae76f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae76f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ae76f-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae76f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae76f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae76f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae76f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae76f-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae76f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae76f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae76f-123">**\_SETOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="ae76f-123">**EM\_SETOPTIONS**</span></span>](em-setoptions.md)
</dt> </dl>

 

 





