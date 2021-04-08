---
title: Message PSM_SETNEXTTEXT (Prsht. h)
description: Définit le texte du bouton suivant dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740093"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="743e3-105">\_Message PSM SETNEXTTEXT</span><span class="sxs-lookup"><span data-stu-id="743e3-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="743e3-106">Définit le texte du bouton **suivant** dans un Assistant.</span><span class="sxs-lookup"><span data-stu-id="743e3-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="743e3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .</span><span class="sxs-lookup"><span data-stu-id="743e3-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="743e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="743e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="743e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="743e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="743e3-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="743e3-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="743e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="743e3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="743e3-112">Pointeur vers une mémoire tampon qui contient le texte.</span><span class="sxs-lookup"><span data-stu-id="743e3-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="743e3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="743e3-113">Return value</span></span>

<span data-ttu-id="743e3-114">Aucune valeur de retour significative.</span><span class="sxs-lookup"><span data-stu-id="743e3-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="743e3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="743e3-115">Requirements</span></span>



| <span data-ttu-id="743e3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="743e3-116">Requirement</span></span> | <span data-ttu-id="743e3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="743e3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="743e3-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="743e3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="743e3-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="743e3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="743e3-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="743e3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="743e3-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="743e3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="743e3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="743e3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="743e3-123"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="743e3-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="743e3-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="743e3-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="743e3-125">**PSM \_ SETNEXTTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="743e3-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 





