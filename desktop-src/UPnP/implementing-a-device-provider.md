---
title: Implémentation d’un fournisseur d’appareils
description: Pour implémenter un fournisseur d’appareils, créez un objet qui expose l’interface IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462450"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="e0da8-103">Implémentation d’un fournisseur d’appareils</span><span class="sxs-lookup"><span data-stu-id="e0da8-103">Implementing a Device Provider</span></span>

<span data-ttu-id="e0da8-104">Pour implémenter un fournisseur d’appareils, créez un objet qui expose l’interface [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="e0da8-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="e0da8-105">Cet objet doit être inscrit auprès de l’hôte d’appareil à l’aide de la méthode [**IUPnPRegistrar :: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="e0da8-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="e0da8-106">Cette méthode accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e0da8-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="e0da8-107">Nom du fournisseur, qui doit être unique sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e0da8-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="e0da8-108">ProgID de la classe qui implémente le fournisseur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e0da8-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="e0da8-109">Chaîne d’initialisation qui est passée au fournisseur de l’appareil au démarrage.</span><span class="sxs-lookup"><span data-stu-id="e0da8-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="e0da8-110">ID de conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0da8-110">A container ID.</span></span> <span data-ttu-id="e0da8-111">Un ID de conteneur est une chaîne qui identifie le groupe auquel appartient l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e0da8-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="e0da8-112">Tous les appareils avec le même identificateur de conteneur sont hébergés dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="e0da8-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




