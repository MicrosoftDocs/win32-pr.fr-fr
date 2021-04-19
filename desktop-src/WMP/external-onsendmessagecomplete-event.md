---
title: External. OnSendMessageComplete, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnSendMessageComplete, événement
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Événement External. OnSendMessageComplete lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539513"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="78489-105">External. OnSendMessageComplete, événement</span><span class="sxs-lookup"><span data-stu-id="78489-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="78489-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="78489-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="78489-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="78489-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="78489-108">L’événement **OnSendMessageComplete** se produit lorsque le magasin en ligne a terminé le traitement d’un message.</span><span class="sxs-lookup"><span data-stu-id="78489-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="78489-109">Le script sur la page de découverte a précédemment envoyé le message en appelant [External. SendMessage](external-sendmessage.md).</span><span class="sxs-lookup"><span data-stu-id="78489-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="78489-110">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="78489-110">Possible Values</span></span>

<span data-ttu-id="78489-111">Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.</span><span class="sxs-lookup"><span data-stu-id="78489-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="78489-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78489-112">Parameters</span></span>

<span data-ttu-id="78489-113">La fonction qui gère cet événement a les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="78489-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="78489-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Fragment*</span><span class="sxs-lookup"><span data-stu-id="78489-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="78489-115">La même chaîne qui a été passée dans le paramètre **MSG** de **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="78489-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="78489-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Envoyés*</span><span class="sxs-lookup"><span data-stu-id="78489-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="78489-117">La même chaîne qui a été passée dans le paramètre **param** de **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="78489-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="78489-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Venir*</span><span class="sxs-lookup"><span data-stu-id="78489-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="78489-119">**Chaîne** qui contient le résultat de la gestion des messages.</span><span class="sxs-lookup"><span data-stu-id="78489-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="78489-120">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="78489-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78489-121">Notes</span><span class="sxs-lookup"><span data-stu-id="78489-121">Remarks</span></span>

<span data-ttu-id="78489-122">La méthode **SendMessage** appelle [IWMPContentPartner :: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), qui retourne de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="78489-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="78489-123">Autrement dit, il retourne avant que le magasin en ligne ne termine le traitement du message.</span><span class="sxs-lookup"><span data-stu-id="78489-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="78489-124">Lorsque le magasin en ligne a terminé le traitement du message, il appelle [IWMPContentPartnerCallback :: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), qui à son tour appelle le gestionnaire d’événements **OnSendMessageComplete** du script.</span><span class="sxs-lookup"><span data-stu-id="78489-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="78489-125">Lorsque le magasin en ligne appelle **IWMPContentPartnerCallback :: SendMessageComplete**, il fournit un code de résultat dans le paramètre *bstrResult* .</span><span class="sxs-lookup"><span data-stu-id="78489-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="78489-126">Le lecteur Windows Media n’interprète pas ce code de résultat.</span><span class="sxs-lookup"><span data-stu-id="78489-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="78489-127">Au lieu de cela, le lecteur Windows Media transmet le code de résultat au gestionnaire d’événements **OnSendMessageComplete** dans le paramètre de *résultat* .</span><span class="sxs-lookup"><span data-stu-id="78489-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="78489-128">Aucun des paramètres (*MSG*, *param*, *result*) du gestionnaire d’événements **OnSendMessageComplete** n’est interprété par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="78489-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="78489-129">Les paramètres n’ont de sens que dans le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="78489-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="78489-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78489-130">Requirements</span></span>



| <span data-ttu-id="78489-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78489-131">Requirement</span></span> | <span data-ttu-id="78489-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="78489-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78489-133">Version</span><span class="sxs-lookup"><span data-stu-id="78489-133">Version</span></span><br/> | <span data-ttu-id="78489-134">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="78489-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="78489-135">DLL</span><span class="sxs-lookup"><span data-stu-id="78489-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="78489-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78489-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78489-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78489-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78489-138">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="78489-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="78489-139">**External. sendMessage**</span><span class="sxs-lookup"><span data-stu-id="78489-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="78489-140">**IWMPContentPartner :: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="78489-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="78489-141">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="78489-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





