---
title: Message EM_SETCARETINDEX (CommCtrl. h)
description: Définit la valeur d’index de base zéro de la position du signe insertion dans un contrôle d’édition.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466550"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="4f512-104">\_Message SETCARETINDEX em</span><span class="sxs-lookup"><span data-stu-id="4f512-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="4f512-105">Définit la valeur d’index de base zéro de la position du signe insertion dans un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4f512-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f512-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f512-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f512-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f512-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f512-108">Nouvelle valeur d’index de base zéro de la position du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="4f512-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="4f512-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f512-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4f512-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4f512-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f512-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f512-111">Return value</span></span>

<span data-ttu-id="4f512-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4f512-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f512-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4f512-113">Remarks</span></span>

<span data-ttu-id="4f512-114">Si l’index est en dehors de la plage du texte d’un contrôle d’édition, l’index est ajusté pour s’ajuster à la plage du texte.</span><span class="sxs-lookup"><span data-stu-id="4f512-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f512-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f512-115">Requirements</span></span>



| <span data-ttu-id="4f512-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f512-116">Requirement</span></span> | <span data-ttu-id="4f512-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f512-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f512-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f512-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f512-119">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f512-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4f512-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f512-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f512-121">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f512-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4f512-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f512-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f512-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f512-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f512-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f512-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="4f512-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4f512-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4f512-126">**\_GETCARETINDEX em**</span><span class="sxs-lookup"><span data-stu-id="4f512-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 





