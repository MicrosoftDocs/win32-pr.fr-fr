---
title: Message EM_GETIMECOMPMODE (RichEdit. h)
description: Récupère le mode IME (éditeur de méthode d’entrée) actuel pour un contrôle RichEdit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466106"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="cf0bd-104">\_Message GETIMECOMPMODE em</span><span class="sxs-lookup"><span data-stu-id="cf0bd-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="cf0bd-105">Récupère le mode IME (éditeur de méthode d’entrée) actuel pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf0bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf0bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0bd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf0bd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf0bd-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cf0bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf0bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf0bd-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf0bd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf0bd-111">Return value</span></span>

<span data-ttu-id="cf0bd-112">La valeur de retour est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="cf0bd-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cf0bd-113">Return code</span></span>                                                                                     | <span data-ttu-id="cf0bd-114">Description</span><span class="sxs-lookup"><span data-stu-id="cf0bd-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="cf0bd-115"><dt>**\_NOTOPEN ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="cf0bd-116">L’IME n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="cf0bd-117"><dt>**\_NIVEAU3 ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="cf0bd-118">Mode inline réel.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="cf0bd-119"><dt>**Le \_ d’isolement2**</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="cf0bd-120">Niveau 2.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="cf0bd-121"><dt>**ICM- \_ d’isolement2 \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="cf0bd-122">Niveau 2,5</span><span class="sxs-lookup"><span data-stu-id="cf0bd-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="cf0bd-123"><dt>**CCI \_ d’isolement2- \_ sui**</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="cf0bd-124">Interface utilisateur spéciale.</span><span class="sxs-lookup"><span data-stu-id="cf0bd-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="cf0bd-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf0bd-125">Requirements</span></span>



| <span data-ttu-id="cf0bd-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf0bd-126">Requirement</span></span> | <span data-ttu-id="cf0bd-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf0bd-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0bd-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf0bd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0bd-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf0bd-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf0bd-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf0bd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0bd-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf0bd-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf0bd-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf0bd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf0bd-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf0bd-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





