---
title: Message PSM_QUERYSIBLINGS (Prsht. h)
description: Envoyé à une feuille de propriétés, qui transfère ensuite le message à chacune de ses pages. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508701"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="c0a2a-105">\_Message PSM QUERYSIBLINGS</span><span class="sxs-lookup"><span data-stu-id="c0a2a-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="c0a2a-106">Envoyé à une feuille de propriétés, qui transfère ensuite le message à chacune de ses pages.</span><span class="sxs-lookup"><span data-stu-id="c0a2a-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="c0a2a-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .</span><span class="sxs-lookup"><span data-stu-id="c0a2a-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0a2a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0a2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a2a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0a2a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0a2a-110">Premier paramètre défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="c0a2a-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0a2a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0a2a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0a2a-112">Deuxième paramètre défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="c0a2a-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0a2a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0a2a-113">Return value</span></span>

<span data-ttu-id="c0a2a-114">Retourne la valeur différente de zéro d’une page de la feuille de propriétés, ou zéro si aucune page ne retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c0a2a-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0a2a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c0a2a-115">Remarks</span></span>

<span data-ttu-id="c0a2a-116">Si une page retourne une valeur différente de zéro, la feuille de propriétés n’envoie pas le message aux pages suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0a2a-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a2a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0a2a-117">Requirements</span></span>



| <span data-ttu-id="c0a2a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0a2a-118">Requirement</span></span> | <span data-ttu-id="c0a2a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0a2a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a2a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0a2a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a2a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0a2a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c0a2a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0a2a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a2a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0a2a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0a2a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0a2a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0a2a-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a2a-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





