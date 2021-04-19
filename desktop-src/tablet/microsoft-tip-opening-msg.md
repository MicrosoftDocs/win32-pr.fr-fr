---
description: Avertit la fenêtre de l’ouverture du panneau de saisie de texte.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Message MICROSOFT_TIP_OPENING_MSG (PenInputPanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530023"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="58c14-103">\_Conseil Microsoft \_ ouverture du \_ message MSG</span><span class="sxs-lookup"><span data-stu-id="58c14-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="58c14-104">Avertit la fenêtre de l’ouverture du panneau de saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="58c14-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="58c14-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58c14-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c14-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58c14-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58c14-107">N’est pas utilisé actuellement, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="58c14-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="58c14-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58c14-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58c14-109">N’est pas utilisé actuellement, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="58c14-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c14-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58c14-110">Return value</span></span>

<span data-ttu-id="58c14-111">Les applications doivent appeler [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) après le traitement de ce message.</span><span class="sxs-lookup"><span data-stu-id="58c14-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="58c14-112">Pour plus d’informations sur les valeurs de retour, consultez **DefWindowProc** .</span><span class="sxs-lookup"><span data-stu-id="58c14-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="58c14-113">Notes</span><span class="sxs-lookup"><span data-stu-id="58c14-113">Remarks</span></span>

<span data-ttu-id="58c14-114">Cette notification vous permet de savoir à quel moment le panneau de saisie s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="58c14-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="58c14-115">Si vous souhaitez exécuter une action lorsque cela se produit, gérez le message, effectuez votre opération dans le gestionnaire, puis transmettez le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="58c14-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="58c14-116">Ce message est également envoyé lorsque le panneau de saisie de texte est déjà visible et que l’utilisateur passe du clavier à l’apparence d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="58c14-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58c14-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58c14-117">Requirements</span></span>



| <span data-ttu-id="58c14-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58c14-118">Requirement</span></span> | <span data-ttu-id="58c14-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="58c14-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c14-120">Client</span><span class="sxs-lookup"><span data-stu-id="58c14-120">Client</span></span><br/> | <span data-ttu-id="58c14-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58c14-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="58c14-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="58c14-122">Header</span></span><br/> | <dl> <span data-ttu-id="58c14-123"><dt>PenInputPanel. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c14-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 

