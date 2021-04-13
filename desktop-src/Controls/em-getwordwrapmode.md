---
title: Message EM_GETWORDWRAPMODE (RichEdit. h)
description: Obtient le retour automatique à la ligne et les options de saut de mot en cours pour le contrôle RichEdit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464542"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="1b155-104">\_Message GETWORDWRAPMODE em</span><span class="sxs-lookup"><span data-stu-id="1b155-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="1b155-105">Obtient le retour automatique à la ligne et les options de saut de mot en cours pour le contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="1b155-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="1b155-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="1b155-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="1b155-107">Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.</span><span class="sxs-lookup"><span data-stu-id="1b155-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="1b155-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b155-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b155-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b155-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b155-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b155-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1b155-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b155-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b155-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b155-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b155-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b155-113">Return value</span></span>

<span data-ttu-id="1b155-114">Le message retourne les options retour automatique à la ligne et saut de mot en cours.</span><span class="sxs-lookup"><span data-stu-id="1b155-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b155-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1b155-115">Remarks</span></span>

<span data-ttu-id="1b155-116">Ce message ne doit pas être envoyé par la procédure de césure définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="1b155-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b155-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b155-117">Requirements</span></span>



| <span data-ttu-id="1b155-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b155-118">Requirement</span></span> | <span data-ttu-id="1b155-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b155-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b155-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b155-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b155-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b155-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b155-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b155-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b155-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b155-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b155-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b155-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b155-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b155-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





