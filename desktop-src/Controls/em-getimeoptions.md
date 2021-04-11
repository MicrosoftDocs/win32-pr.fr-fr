---
title: Message EM_GETIMEOPTIONS (RichEdit. h)
description: Récupère les options de l’éditeur de méthode d’entrée (IME) en cours.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104821"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="7a2d4-104">\_Message GETIMEOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="7a2d4-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="7a2d4-105">Récupère les options de l’éditeur de méthode d’entrée (IME) en cours.</span><span class="sxs-lookup"><span data-stu-id="7a2d4-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="7a2d4-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="7a2d4-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="7a2d4-107">Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.</span><span class="sxs-lookup"><span data-stu-id="7a2d4-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="7a2d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a2d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a2d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a2d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a2d4-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7a2d4-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7a2d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a2d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a2d4-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7a2d4-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a2d4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a2d4-113">Return value</span></span>

<span data-ttu-id="7a2d4-114">Ce message retourne une ou plusieurs des valeurs d’indicateur d’option IME décrites dans le message [**em \_ SETIMEOPTIONS**](em-setimeoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2d4-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2d4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a2d4-115">Requirements</span></span>



| <span data-ttu-id="7a2d4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a2d4-116">Requirement</span></span> | <span data-ttu-id="7a2d4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a2d4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2d4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a2d4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2d4-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a2d4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a2d4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a2d4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a2d4-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a2d4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a2d4-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a2d4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a2d4-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a2d4-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a2d4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a2d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2d4-125">**\_SETIMEOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="7a2d4-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





