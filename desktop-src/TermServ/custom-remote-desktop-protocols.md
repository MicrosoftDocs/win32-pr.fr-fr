---
title: API du fournisseur protocole RDP (Remote Desktop Protocol)
description: Vous utilisez l’API du fournisseur protocole RDP (Remote Desktop Protocol) pour créer un protocole pour assurer la communication entre le service Services Bureau à distance et plusieurs clients.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939553"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="b1546-103">API du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="b1546-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="b1546-104">Vous utilisez l’API du fournisseur protocole RDP (Remote Desktop Protocol) pour créer un protocole pour assurer la communication entre le service Services Bureau à distance et plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="b1546-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="b1546-105">Lorsque Windows Server se charge, le service Services Bureau à distance (également appelé gestionnaire de connexion à distance (RCM)) démarre.</span><span class="sxs-lookup"><span data-stu-id="b1546-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="b1546-106">Le service démarre également les objets d’écouteur pour les fournisseurs de protocole RDP (Remote Desktop Protocol) qui, à leur tour, écoutent les connexions clientes.</span><span class="sxs-lookup"><span data-stu-id="b1546-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="b1546-107">Le service et les fournisseurs de protocole sont des objets en mode utilisateur qui communiquent à l’aide des API abordées dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="b1546-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="b1546-108">Les fournisseurs de protocole peuvent communiquer avec les pilotes en mode noyau en utilisant des contrôles d’entrée/sortie (IOCTL).</span><span class="sxs-lookup"><span data-stu-id="b1546-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="b1546-109">L'illustration ci-dessous décrit cela.</span><span class="sxs-lookup"><span data-stu-id="b1546-109">This is shown in the following illustration.</span></span>

![architecture de l’API de protocole personnalisé](images/protocol-architecture.png)

<span data-ttu-id="b1546-111">Microsoft a implémenté le protocole RDP (Remote Desktop Protocol) (RDP) pour assurer la communication entre le service Services Bureau à distance et les connexions clientes.</span><span class="sxs-lookup"><span data-stu-id="b1546-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="b1546-112">Vous pouvez créer votre propre protocole à l’aide des interfaces, structures, unions et types d’énumération qui composent l’API du fournisseur protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="b1546-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="b1546-113">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b1546-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="b1546-114">Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="b1546-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="b1546-115">Informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="b1546-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="b1546-116">Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.</span><span class="sxs-lookup"><span data-stu-id="b1546-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="b1546-117">Référence du fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="b1546-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="b1546-118">Contient des interfaces, des structures, des unions et des types énumération qui vous permettent de créer un protocole RDP (Remote Desktop Protocol) personnalisé (RDP).</span><span class="sxs-lookup"><span data-stu-id="b1546-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b1546-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1546-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1546-120">À propos de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b1546-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




