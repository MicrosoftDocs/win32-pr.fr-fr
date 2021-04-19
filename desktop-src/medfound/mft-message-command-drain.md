---
description: Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517001"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="b22be-103">\_drain de \_ commande de message MFT \_</span><span class="sxs-lookup"><span data-stu-id="b22be-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="b22be-104">Demande à une transformation de Media Foundation (MFT) de vider toutes les données stockées.</span><span class="sxs-lookup"><span data-stu-id="b22be-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="b22be-105">Paramètre de message</span><span class="sxs-lookup"><span data-stu-id="b22be-105">Message Parameter</span></span>

<span data-ttu-id="b22be-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b22be-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b22be-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b22be-107">Remarks</span></span>

<span data-ttu-id="b22be-108">Pour envoyer ce message, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="b22be-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="b22be-109">Après l’envoi de ce message, le flux d’entrée spécifié n’accepte pas d’entrée tant que la table MFT n’a pas traité toutes les données des appels précédents à [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="b22be-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="b22be-110">Le processus de drainage varie légèrement entre les MFTs synchrones et les MFTs asynchrones :</span><span class="sxs-lookup"><span data-stu-id="b22be-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="b22be-111">**MFTs synchrone**</span><span class="sxs-lookup"><span data-stu-id="b22be-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="b22be-112">Une fois que le client a envoyé ce message, il appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) dans une boucle, jusqu’à ce que **ProcessOutput** retourne le code **d’erreur MF \_ E \_ Transform \_ nécessite \_ plus \_ d’entrée**.</span><span class="sxs-lookup"><span data-stu-id="b22be-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="b22be-113">Tant que la table MFT a toujours des données à traiter, les appels ultérieurs à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) échouent.</span><span class="sxs-lookup"><span data-stu-id="b22be-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="b22be-114">La table MFT continue à produire la sortie jusqu’à ce qu’elle utilise toutes les données stockées.</span><span class="sxs-lookup"><span data-stu-id="b22be-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="b22be-115">La table MFT ignore toutes les données qui ne peuvent pas être traitées dans un exemple complet de sortie.</span><span class="sxs-lookup"><span data-stu-id="b22be-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="b22be-116">(Par exemple, il doit supprimer une image vidéo partielle.)</span><span class="sxs-lookup"><span data-stu-id="b22be-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="b22be-117">**MFTs asynchrone**</span><span class="sxs-lookup"><span data-stu-id="b22be-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="b22be-118">La table MFT continue à envoyer des événements [METransformHaveOutput](metransformhaveoutput.md) jusqu’à ce qu’elle n’ait plus aucune donnée à traiter.</span><span class="sxs-lookup"><span data-stu-id="b22be-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="b22be-119">Elle n’envoie pas d’événements [METransformNeedInput](metransformneedinput.md) pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="b22be-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="b22be-120">Une fois que la table MFT envoie le dernier événement [METransformHaveOutput](metransformhaveoutput.md) , elle envoie un événement [METransformDrainComplete](metransformdraincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="b22be-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="b22be-121">Une fois l’opération de drainage terminée, la table MFT n’envoie pas d’autre événement [METransformNeedInput](metransformneedinput.md) tant qu’elle n’a pas reçu de message [**MFT \_ message \_ \_ \_ de démarrage de \_ flux**](mft-message-notify-start-of-stream.md) du client.</span><span class="sxs-lookup"><span data-stu-id="b22be-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="b22be-122">Une fois que le client a vidé la MFT, le client peut envoyer plus de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b22be-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="b22be-123">Le premier échantillon après l’opération de drainage doit avoir l’attribut discontinu ([**MFSampleExtension \_ discontinu**](mfsampleextension-discontinuity-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="b22be-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="b22be-124">Les versions antérieures de cette documentation indiquaient que le paramètre d’événement *ulParam* est membre de l’énumération du [**\_ \_ \_ type de drainage MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) .</span><span class="sxs-lookup"><span data-stu-id="b22be-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="b22be-125">C’est inexact.</span><span class="sxs-lookup"><span data-stu-id="b22be-125">That is not correct.</span></span> <span data-ttu-id="b22be-126">*UlParam* contient un identificateur de flux.</span><span class="sxs-lookup"><span data-stu-id="b22be-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="b22be-127">Implémentation</span><span class="sxs-lookup"><span data-stu-id="b22be-127">Implementation</span></span>

<span data-ttu-id="b22be-128">Une table MFT asynchrone doit toujours retourner [METransformDrainComplete](metransformdraincomplete.md) une fois qu’elle a été vidée.</span><span class="sxs-lookup"><span data-stu-id="b22be-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="b22be-129">Une table MFT synchrone peut ignorer ce message et retourner \_ la valeur OK si les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="b22be-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="b22be-130">La table MFT ne stocke jamais plus d’un échantillon d’entrée à la fois.</span><span class="sxs-lookup"><span data-stu-id="b22be-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="b22be-131">Chaque exemple d’entrée produit un seul échantillon de sortie.</span><span class="sxs-lookup"><span data-stu-id="b22be-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="b22be-132">Dans le cas contraire, un MFT synchrone doit implémenter ce message.</span><span class="sxs-lookup"><span data-stu-id="b22be-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22be-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b22be-133">Requirements</span></span>



| <span data-ttu-id="b22be-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b22be-134">Requirement</span></span> | <span data-ttu-id="b22be-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b22be-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b22be-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b22be-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b22be-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b22be-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b22be-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b22be-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b22be-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b22be-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b22be-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b22be-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22be-141"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b22be-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22be-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b22be-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22be-143">**\_type de message MFT \_**</span><span class="sxs-lookup"><span data-stu-id="b22be-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="b22be-144">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="b22be-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




