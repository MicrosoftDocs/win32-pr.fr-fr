---
title: Interfaces du fournisseur protocole RDP (Remote Desktop Protocol)
description: Interfaces prises en charge par l’API du fournisseur protocole RDP (Remote Desktop Protocol).
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939552"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="f1e5f-103">Interfaces du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="f1e5f-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="f1e5f-104">Les interfaces suivantes sont prises en charge par l’API du fournisseur protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="f1e5f-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1e5f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f1e5f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f1e5f-106">**IWRdsProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="f1e5f-107">Expose les méthodes appelées par le service Services Bureau à distance pour configurer une connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-108">**IWRdsProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="f1e5f-109">Expose des méthodes qui fournissent des informations sur l’état d’une connexion cliente et qui effectuent des actions pour le client.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="f1e5f-110">Cette interface est implémentée par le service Services Bureau à distance et appelée par le protocole.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-111">**IWRdsProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="f1e5f-112">Expose les méthodes utilisées par le service Services Bureau à distance pour exécuter le protocole de transfert de licences pendant une séquence de connexion.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-113">**IWRdsProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="f1e5f-114">Expose des méthodes qui demandent que le protocole démarre et cesse d’écouter les demandes de connexion clientes.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-115">**IWRdsProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="f1e5f-116">Expose des méthodes qui informent le service Services Bureau à distance qu’un client s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-117">**IWRdsProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="f1e5f-118">Expose les méthodes appelées par le service Services Bureau à distance pour mettre à jour l’état de l’ouverture de session et déterminer comment diriger les messages d’erreur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-119">**IWRdsProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="f1e5f-120">Expose les méthodes que le service Services Bureau à distance utilise pour communiquer avec le fournisseur de protocole.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-121">**IWRdsProtocolSettings**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="f1e5f-122">Expose des méthodes pour récupérer et ajouter des paramètres liés à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-123">**IWRdsProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="f1e5f-124">Expose les méthodes appelées par le protocole pour notifier au service Services Bureau à distance de démarrer ou d’arrêter le côté cible d’une ombre.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-125">**IWRdsProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="f1e5f-126">Expose des méthodes qui informent le fournisseur de protocole de l’état de l’occultation de session.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-127">**IWRdsRemoteFXGraphicsConnection**</span><span class="sxs-lookup"><span data-stu-id="f1e5f-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="f1e5f-128">Expose des méthodes relatives à la manipulation et à la compréhension des graphiques sur la connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="f1e5f-129">Interfaces du fournisseur de protocole Desktop déconseillées</span><span class="sxs-lookup"><span data-stu-id="f1e5f-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="f1e5f-130">Les interfaces suivantes sont déconseillées et ne doivent plus être utilisées.</span><span class="sxs-lookup"><span data-stu-id="f1e5f-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="f1e5f-131">Pour les nouveaux projets, utilisez à la place les interfaces des interfaces du fournisseur protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="f1e5f-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f1e5f-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1e5f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e5f-133">Référence du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="f1e5f-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="f1e5f-134">Énumérations du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="f1e5f-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="f1e5f-135">Structures du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="f1e5f-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="f1e5f-136">Unions de fournisseurs protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="f1e5f-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




