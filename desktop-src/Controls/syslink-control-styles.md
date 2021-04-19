---
title: Styles de contrôle SysLink (CommCtrl. h)
description: Les constantes de style suivantes sont utilisées lors de la création de contrôles SysLink.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545455"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="6c722-103">Styles de contrôle SysLink</span><span class="sxs-lookup"><span data-stu-id="6c722-103">SysLink Control Styles</span></span>

<span data-ttu-id="6c722-104">Les constantes de style suivantes sont utilisées lors de la création de contrôles SysLink.</span><span class="sxs-lookup"><span data-stu-id="6c722-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="6c722-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6c722-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="6c722-106">Description</span><span class="sxs-lookup"><span data-stu-id="6c722-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="6c722-107"><dt>**LWS \_ transparent**</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="6c722-108">Le mode de combinaison d’arrière-plan est transparent.</span><span class="sxs-lookup"><span data-stu-id="6c722-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="6c722-109"><dt>**LWS \_ IGNORERETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="6c722-110">Lorsque le lien a le focus clavier et que l’utilisateur appuie sur entrée, la touche est ignorée par le contrôle et transmise à la boîte de dialogue hôte.</span><span class="sxs-lookup"><span data-stu-id="6c722-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="6c722-111"><dt>**le \_ préfixe LWS**</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="6c722-112">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6c722-112">**Windows Vista**.</span></span> <span data-ttu-id="6c722-113">Si le texte contient une esperluette, il est traité comme un caractère littéral plutôt que le préfixe d’une touche de raccourci.</span><span class="sxs-lookup"><span data-stu-id="6c722-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="6c722-114"><dt>**LWS \_ USEVISUALSTYLE**</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="6c722-115">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6c722-115">**Windows Vista**.</span></span> <span data-ttu-id="6c722-116">Le lien est affiché dans le style visuel actuel.</span><span class="sxs-lookup"><span data-stu-id="6c722-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="6c722-117"><dt>**\_USECUSTOMTEXT LWS**</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="6c722-118">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6c722-118">**Windows Vista**.</span></span> <span data-ttu-id="6c722-119">Une [notification \_ CUSTOMTEXT nm](nm-customtext.md) est envoyée lorsque le contrôle est dessiné, afin que l’application puisse fournir du texte de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="6c722-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="6c722-120"><dt>**LWS \_ droit**</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="6c722-121">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6c722-121">**Windows Vista**.</span></span> <span data-ttu-id="6c722-122">Le texte est justifié à droite.</span><span class="sxs-lookup"><span data-stu-id="6c722-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="6c722-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c722-123">Requirements</span></span>



| <span data-ttu-id="6c722-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c722-124">Requirement</span></span> | <span data-ttu-id="6c722-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c722-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c722-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c722-126">Header</span></span><br/> | <dl> <span data-ttu-id="6c722-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





