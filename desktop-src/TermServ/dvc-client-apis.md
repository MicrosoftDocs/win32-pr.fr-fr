---
title: API clientes DVC
description: Les API clientes de canal virtuel dynamique (DVC) sont implémentées spécifiquement pour le client Connexion Bureau à distance (RDC) de la connexion.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309782"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="1b901-103">API clientes DVC</span><span class="sxs-lookup"><span data-stu-id="1b901-103">DVC Client APIs</span></span>

<span data-ttu-id="1b901-104">Les API clientes de canal virtuel dynamique (DVC) sont implémentées spécifiquement pour le client Connexion Bureau à distance (RDC) de la connexion.</span><span class="sxs-lookup"><span data-stu-id="1b901-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="1b901-105">Certaines API sont implémentées par l’infrastructure DVC, et certaines sont implémentées par le développeur du plug-in.</span><span class="sxs-lookup"><span data-stu-id="1b901-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="1b901-106">Certaines API sont utilisées pour prendre en charge le plug-in client Connexion Bureau à distance (RDC) et ne sont pas directement liées au transport de données.</span><span class="sxs-lookup"><span data-stu-id="1b901-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b901-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1b901-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="1b901-108">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="1b901-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="1b901-109">Autorise le chargement du plug-in client Connexion Bureau à distance (RDC) par le client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="1b901-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-110">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="1b901-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="1b901-111">Gère les paramètres de configuration pour chaque écouteur de la connexion de canal virtuel dynamique (DVC).</span><span class="sxs-lookup"><span data-stu-id="1b901-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-112">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="1b901-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="1b901-113">Permet d’informer le plug-in client Connexion Bureau à distance (RDC) des demandes entrantes sur un écouteur particulier.</span><span class="sxs-lookup"><span data-stu-id="1b901-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-114">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="1b901-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="1b901-115">Gère tous les plug-ins client Connexion Bureau à distance (RDC) et les écouteurs de canal virtuel dynamique (DVC).</span><span class="sxs-lookup"><span data-stu-id="1b901-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-116">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="1b901-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="1b901-117">Utilisé pour contrôler l’état du canal et écrit sur le canal.</span><span class="sxs-lookup"><span data-stu-id="1b901-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-118">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="1b901-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="1b901-119">Reçoit des notifications sur les modifications de l’état du canal ou les données reçues.</span><span class="sxs-lookup"><span data-stu-id="1b901-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="1b901-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="1b901-121">Cette interface n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1b901-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="1b901-122">**VirtualChannelGetInstance**</span><span class="sxs-lookup"><span data-stu-id="1b901-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="1b901-123">Appelé pour que le plug-in crée une instance de l’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour tous les plug-ins implémentés par la dll.</span><span class="sxs-lookup"><span data-stu-id="1b901-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




