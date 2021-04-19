---
title: External. OnLoginChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnLoginChange, événement
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Événement External. OnLoginChange lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525136"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="ac627-105">External. OnLoginChange, événement</span><span class="sxs-lookup"><span data-stu-id="ac627-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="ac627-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="ac627-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ac627-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ac627-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ac627-108">L’événement **OnLoginChange** se produit lorsque l’état de la connexion de l’utilisateur change ou lorsqu’une tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="ac627-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="ac627-109">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ac627-109">Possible Values</span></span>

<span data-ttu-id="ac627-110">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="ac627-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac627-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac627-111">Parameters</span></span>

<span data-ttu-id="ac627-112">La fonction qui gère cet événement n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ac627-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac627-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ac627-113">Remarks</span></span>

<span data-ttu-id="ac627-114">Cet événement se produit chaque fois que le plug-in du magasin en ligne appelle [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), en passant wmpcnLoginStateChange dans le paramètre de *type* .</span><span class="sxs-lookup"><span data-stu-id="ac627-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="ac627-115">Parfois, le plug-in effectue cet appel pour notifier le lecteur Windows Media qu’une modification a été apportée à l’état de connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ac627-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="ac627-116">Dans d’autres cas, le plug-in effectue cet appel pour informer le joueur qu’une tentative de connexion a échoué.</span><span class="sxs-lookup"><span data-stu-id="ac627-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="ac627-117">Le paramètre *pContext* de la méthode **Notify** spécifie si la notification est destinée à un changement d’état de connexion ou à une tentative d’ouverture de session qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="ac627-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="ac627-118">Étant donné que chaque appel à `Notify(wmpcnLoginStateChange, ...)` amène le lecteur Windows Media à déclencher l’événement **OnLoginChange** , le gestionnaire d’événements **OnLoginChange** est parfois appelé à la suite d’une modification de l’état de connexion et parfois à la suite d’un échec de tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="ac627-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="ac627-119">Pour déterminer l’état actuel de la connexion de l’utilisateur, le gestionnaire d’événements **OnLoginChange** doit appeler [External. userLoggedIn](external-userloggedin.md).</span><span class="sxs-lookup"><span data-stu-id="ac627-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac627-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac627-120">Requirements</span></span>



| <span data-ttu-id="ac627-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac627-121">Requirement</span></span> | <span data-ttu-id="ac627-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac627-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac627-123">Version</span><span class="sxs-lookup"><span data-stu-id="ac627-123">Version</span></span><br/> | <span data-ttu-id="ac627-124">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="ac627-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="ac627-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac627-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac627-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac627-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac627-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac627-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac627-128">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="ac627-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ac627-129">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="ac627-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="ac627-130">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="ac627-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





