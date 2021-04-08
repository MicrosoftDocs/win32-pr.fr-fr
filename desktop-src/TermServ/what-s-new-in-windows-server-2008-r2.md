---
title: Nouveautés de Windows Server 2008 R2
description: Windows Server 2008 R2 introduit les nouveaux éléments de programmation suivants pour Services Bureau à distance.
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103940638"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="45e68-103">Nouveautés de Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45e68-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="45e68-104">Windows Server 2008 R2 introduit les nouveaux éléments de programmation suivants pour Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="45e68-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45e68-105">Les services Terminal Server sont désormais Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="45e68-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="45e68-106">Les services Terminal Server ont été renommés Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="45e68-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="45e68-107">Un serveur sur lequel est installé le service de rôle hôte de session Bureau à distance (hôte de session Bureau à distance) est maintenant appelé serveur hôte de session Bureau à distance, au lieu d’un serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="45e68-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="45e68-108"><a href="terminal-services-is-now-remote-desktop-services.md">Les services Terminal Server sont désormais Services Bureau à distance</a></span><span class="sxs-lookup"><span data-stu-id="45e68-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e68-109">API de virtualisation Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="45e68-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="45e68-110">L’API de virtualisation Bureau à distance fournit des énumérations, des interfaces et des structures que vous pouvez utiliser pour créer des plug-ins personnalisés qui remplacent la logique de redirection standard de Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="45e68-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="45e68-111">Le Service Broker pour les connexions Bureau à distance (anciennement session Broker TS) a été étendu pour prendre en charge les connexions aux ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="45e68-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="45e68-112"><a href="using-the-remote-desktop-virtualization-api.md">Utilisation de l’API de virtualisation Bureau à distance</a></span><span class="sxs-lookup"><span data-stu-id="45e68-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="45e68-113"><a href="terminal-services-virtualization-api-reference.md">Informations de référence sur l’API de virtualisation Bureau à distance</a></span><span class="sxs-lookup"><span data-stu-id="45e68-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e68-114">Fournisseur protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="45e68-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="45e68-115">L’API du fournisseur protocole RDP (Remote Desktop Protocol) peut être utilisée pour créer un protocole qui personnalise l’interaction entre le service Services Bureau à distance et les clients de bureau.</span><span class="sxs-lookup"><span data-stu-id="45e68-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="45e68-116"><a href="creating-a-custom-remote-protocol.md">Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)</a></span><span class="sxs-lookup"><span data-stu-id="45e68-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="45e68-117"><a href="custom-remote-protocol-reference.md">Référence du fournisseur protocole RDP (Remote Desktop Protocol)</a></span><span class="sxs-lookup"><span data-stu-id="45e68-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45e68-118">API Services Bureau à distance AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="45e68-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="45e68-119">L’API Services Bureau à distance AudioEndpoint prend en charge l’énumération, les interfaces et les structures pour l’inscription du point de terminaison audio et le transport des données.</span><span class="sxs-lookup"><span data-stu-id="45e68-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="45e68-120"><a href="terminal-services-audioendpoint-api-reference.md">Informations de référence sur l’API Services Bureau à distance AudioEndpoint</a></span><span class="sxs-lookup"><span data-stu-id="45e68-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="45e68-121">API du service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="45e68-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="45e68-122">L’API de service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance prend en charge des interfaces et des structures que vous pouvez utiliser pour effectuer un filtrage personnalisé des ressources et fournir une prise en charge des types de fichiers qui ne sont pas pris en charge en mode natif dans Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="45e68-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="45e68-123"><a href="centralized-publishing-api-reference.md">Informations de référence sur l’API de service Administration des connexions aux programmes RemoteApp et aux services Bureau à distance</a></span><span class="sxs-lookup"><span data-stu-id="45e68-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





