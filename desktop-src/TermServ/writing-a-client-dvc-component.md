---
title: Écriture d’un module DVC client
description: Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513673"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="61f4f-103">Écriture d’un module DVC client</span><span class="sxs-lookup"><span data-stu-id="61f4f-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="61f4f-104">Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="61f4f-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="61f4f-105">Le plug-in DVC est une implémentation de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), inscrite en tant qu’objet COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="61f4f-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="61f4f-106">Le plug-in doit être implémenté dans un modèle de thread libre.</span><span class="sxs-lookup"><span data-stu-id="61f4f-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="61f4f-107">L’implémentation du modèle cloisonné n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="61f4f-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="61f4f-108">Voici une liste des interfaces implémentées par des objets instanciés par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="61f4f-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="61f4f-109">Interface</span><span class="sxs-lookup"><span data-stu-id="61f4f-109">Interface</span></span>                                                        | <span data-ttu-id="61f4f-110">Description</span><span class="sxs-lookup"><span data-stu-id="61f4f-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61f4f-111">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="61f4f-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="61f4f-112">Autorise le chargement du plug-in client Connexion Bureau à distance (RDC) par le client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="61f4f-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="61f4f-113">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="61f4f-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="61f4f-114">Avertit le plug-in client Connexion Bureau à distance (RDC) des demandes entrantes sur un écouteur particulier.</span><span class="sxs-lookup"><span data-stu-id="61f4f-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="61f4f-115">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="61f4f-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="61f4f-116">Reçoit des notifications sur les modifications de l’état du canal ou les données reçues.</span><span class="sxs-lookup"><span data-stu-id="61f4f-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="61f4f-117">Chaque instance de cette interface est associée à une instance de [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span><span class="sxs-lookup"><span data-stu-id="61f4f-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="61f4f-118">Voici une liste des interfaces implémentées par des objets instanciés par le client Connexion Bureau à distance (RDC) et faisant partie de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="61f4f-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="61f4f-119">Interface</span><span class="sxs-lookup"><span data-stu-id="61f4f-119">Interface</span></span>                                                      | <span data-ttu-id="61f4f-120">Description</span><span class="sxs-lookup"><span data-stu-id="61f4f-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61f4f-121">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="61f4f-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="61f4f-122">Gère tous les plug-ins client Connexion Bureau à distance (RDC), les écouteurs DVC ou les canaux virtuels statiques.</span><span class="sxs-lookup"><span data-stu-id="61f4f-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="61f4f-123">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="61f4f-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="61f4f-124">Gère les paramètres de configuration pour chaque écouteur de la connexion DVC.</span><span class="sxs-lookup"><span data-stu-id="61f4f-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="61f4f-125">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="61f4f-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="61f4f-126">Contrôle l’état du canal, ainsi que les écritures sur le canal.</span><span class="sxs-lookup"><span data-stu-id="61f4f-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="61f4f-127">L’illustration suivante montre la relation entre le client Connexion Bureau à distance (RDC) et le plug-in client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="61f4f-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![relation entre le client et le plug-in](images/tsclient.png)

 

 





