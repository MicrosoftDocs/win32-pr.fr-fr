---
title: External. sendMessage, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode sendMessage envoie un message au plug-in du magasin en ligne.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- méthode sendMessage lecteur Windows Media
- méthode sendMessage lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, sendMessage, méthode
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525491"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="70228-108">External. sendMessage, méthode</span><span class="sxs-lookup"><span data-stu-id="70228-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="70228-109">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="70228-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="70228-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70228-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="70228-111">La méthode **SendMessage** envoie un message au plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="70228-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="70228-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70228-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="70228-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70228-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70228-114">*Message* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70228-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70228-115">**Chaîne** contenant le message.</span><span class="sxs-lookup"><span data-stu-id="70228-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="70228-116">*Param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70228-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70228-117">**Chaîne** contenant les paramètres associés au message.</span><span class="sxs-lookup"><span data-stu-id="70228-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70228-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70228-118">Return value</span></span>

<span data-ttu-id="70228-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="70228-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70228-120">Notes</span><span class="sxs-lookup"><span data-stu-id="70228-120">Remarks</span></span>

<span data-ttu-id="70228-121">Le message est envoyé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="70228-121">The message is sent asynchronously.</span></span> <span data-ttu-id="70228-122">Autrement dit, cette méthode retourne immédiatement au lieu d’attendre que le message soit traité.</span><span class="sxs-lookup"><span data-stu-id="70228-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="70228-123">Lorsque le plug-in termine le traitement du message, il appelle la méthode [IWMPContentPartnerCallback :: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , qui à son tour appelle le gestionnaire d’événements [OnSendMessageComplete](external-onsendmessagecomplete-event.md) du script.</span><span class="sxs-lookup"><span data-stu-id="70228-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="70228-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70228-124">Requirements</span></span>



| <span data-ttu-id="70228-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70228-125">Requirement</span></span> | <span data-ttu-id="70228-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="70228-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70228-127">Version</span><span class="sxs-lookup"><span data-stu-id="70228-127">Version</span></span><br/> | <span data-ttu-id="70228-128">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="70228-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="70228-129">DLL</span><span class="sxs-lookup"><span data-stu-id="70228-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="70228-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70228-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70228-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70228-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70228-132">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="70228-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="70228-133">**External. OnSendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="70228-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="70228-134">**IWMPContentPartner :: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="70228-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="70228-135">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="70228-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





