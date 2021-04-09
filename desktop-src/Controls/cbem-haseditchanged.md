---
title: Message CBEM_HASEDITCHANGED (commctrl. h)
description: Détermine si l’utilisateur a modifié le texte d’un contrôle d’édition ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942852"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="ccdd1-104">\_Message CBEM HASEDITCHANGED</span><span class="sxs-lookup"><span data-stu-id="ccdd1-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="ccdd1-105">Détermine si l’utilisateur a modifié le texte d’un contrôle d’édition ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccdd1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccdd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccdd1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccdd1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ccdd1-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ccdd1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccdd1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ccdd1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccdd1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccdd1-111">Return value</span></span>

<span data-ttu-id="ccdd1-112">Retourne la **valeur true** si le texte de la zone d’édition du contrôle a été modifié, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccdd1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ccdd1-113">Remarks</span></span>

<span data-ttu-id="ccdd1-114">Un contrôle ComboBoxEx utilise un contrôle de zone d’édition lorsqu’il est défini sur le style de [**\_ liste déroulante CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdd1-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="ccdd1-115">Vous pouvez récupérer le handle de fenêtre du contrôle de zone d’édition en envoyant un message [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdd1-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="ccdd1-116">Lorsque l’utilisateur commence à modifier, vous recevrez une notification [CBEN \_ BEGINEDIT](cben-beginedit.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdd1-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="ccdd1-117">Une fois la modification terminée ou le focus modifié, vous recevrez une notification [CBEN \_ ENDEDIT](cben-endedit.md) .</span><span class="sxs-lookup"><span data-stu-id="ccdd1-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="ccdd1-118">Le message **CBEM \_ HASEDITCHANGED** n’est utile que pour déterminer si le texte a été modifié s’il est envoyé avant la \_ notification CBEN ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="ccdd1-119">Si le message est envoyé par la suite, la **valeur false** est retournée.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="ccdd1-120">Par exemple, supposons que l’utilisateur commence à modifier le texte dans la zone d’édition, mais qu’il change le focus, générant une \_ notification CBEN ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="ccdd1-121">Si vous envoyez ensuite un message **CBEM \_ HASEDITCHANGED** , la **valeur false** est retournée, même si le texte a été modifié.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="ccdd1-122">Le [**style \_ simple CBS**](combo-box-styles.md) ne fonctionne pas correctement avec **CBEM \_ HASEDITCHANGED**.</span><span class="sxs-lookup"><span data-stu-id="ccdd1-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccdd1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccdd1-123">Requirements</span></span>



| <span data-ttu-id="ccdd1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccdd1-124">Requirement</span></span> | <span data-ttu-id="ccdd1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccdd1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccdd1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccdd1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ccdd1-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccdd1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccdd1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccdd1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ccdd1-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccdd1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccdd1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccdd1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccdd1-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccdd1-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





