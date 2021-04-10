---
description: Détails des événements de suivi Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Événements de suivi Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112987"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="61d83-103">Événements de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="61d83-103">Winsock Tracing Events</span></span>

<span data-ttu-id="61d83-104">Cette section fournit des informations détaillées sur les détails spécifiques des événements de suivi Winsock.</span><span class="sxs-lookup"><span data-stu-id="61d83-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="61d83-105">Le suivi Winsock est une fonctionnalité de résolution des problèmes qui peut être activée dans les binaires de la version commerciale pour suivre certains événements Windows Socket avec une surcharge minimale.</span><span class="sxs-lookup"><span data-stu-id="61d83-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="61d83-106">Cette fonctionnalité permet de meilleures fonctionnalités de diagnostic pour les développeurs et le support technique.</span><span class="sxs-lookup"><span data-stu-id="61d83-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="61d83-107">Le suivi d’événements réseau Winsock prend en charge le suivi des opérations de socket pour les applications IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="61d83-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="61d83-108">Le suivi des modifications du catalogue Winsock prend en charge le suivi des modifications apportées au catalogue Winsock par les fournisseurs de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="61d83-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="61d83-109">Les fournisseurs de services en couche sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="61d83-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="61d83-110">À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="61d83-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="61d83-111">Le suivi Winsock utilise Suivi d’v nements pour Windows (ETW), une fonctionnalité de traçage à usage général et à haut débit fournie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="61d83-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="61d83-112">ETW fournit un mécanisme de suivi pour les événements déclenchés par les applications en mode utilisateur et les pilotes de périphérique en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="61d83-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="61d83-113">ETW permet d’activer et de désactiver la journalisation dynamique, ce qui facilite l’exécution du suivi détaillé dans les environnements de production sans nécessiter de redémarrage ou de redémarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="61d83-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="61d83-114">La prise en charge du suivi Winsock à l’aide d’ETW a été ajoutée sur Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="61d83-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="61d83-115">Pour obtenir des informations générales sur ETW, consultez [améliorer le débogage et le réglage des performances avec ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="61d83-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="61d83-116">La liste suivante fournit des informations détaillées pour chaque événement de suivi Winsock.</span><span class="sxs-lookup"><span data-stu-id="61d83-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="61d83-117">Pour plus d’informations sur les événements, cliquez sur le nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="61d83-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="61d83-118">Nom de l'événement</span><span class="sxs-lookup"><span data-stu-id="61d83-118">Event Name</span></span>                                                            | <span data-ttu-id="61d83-119">Description</span><span class="sxs-lookup"><span data-stu-id="61d83-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61d83-120">**\_création d’événement AFD \_**</span><span class="sxs-lookup"><span data-stu-id="61d83-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="61d83-121">Événement de traçage réseau Winsock pour une opération de création de Socket.</span><span class="sxs-lookup"><span data-stu-id="61d83-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="61d83-122">**fermeture de l' \_ événement AFD \_**</span><span class="sxs-lookup"><span data-stu-id="61d83-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="61d83-123">Événement de traçage réseau Winsock pour l’opération de fermeture du Socket.</span><span class="sxs-lookup"><span data-stu-id="61d83-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="61d83-124">**\_Installation de ws2help \_ LSP \_ Winsock**</span><span class="sxs-lookup"><span data-stu-id="61d83-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="61d83-125">Événement de modification du catalogue Winsock pour une opération d’installation d’un fournisseur de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="61d83-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="61d83-126">**Désinstallation de WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="61d83-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="61d83-127">Événement de modification du catalogue Winsock pour une opération de suppression du fournisseur de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="61d83-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="61d83-128">**Désactivation de WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="61d83-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="61d83-129">Événement de modification du catalogue Winsock pour une opération de désactivation du fournisseur de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="61d83-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="61d83-130">**Réinitialisation de WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="61d83-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="61d83-131">Événement de modification du catalogue Winsock pour une opération de réinitialisation du catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="61d83-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="61d83-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61d83-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61d83-133">Améliorer le débogage et le réglage des performances à l'aide du suivi ETW</span><span class="sxs-lookup"><span data-stu-id="61d83-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="61d83-134">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="61d83-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="61d83-135">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="61d83-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="61d83-136">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="61d83-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="61d83-137">Détails du suivi d’événements réseau Winsock</span><span class="sxs-lookup"><span data-stu-id="61d83-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="61d83-138">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="61d83-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
