---
description: Le fournisseur d’espace de noms PNRP (Peer Name Resolution Protocol) est une technologie de résolution de noms sans serveur qui permet aux nœuds de se découvrir mutuellement.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: À propos de PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115586"
---
# <a name="about-pnrp"></a><span data-ttu-id="f3702-103">À propos de PNRP</span><span class="sxs-lookup"><span data-stu-id="f3702-103">About PNRP</span></span>

<span data-ttu-id="f3702-104">Le fournisseur d’espace de noms PNRP (Peer Name Resolution Protocol) est une technologie de résolution de noms sans serveur qui permet aux nœuds de se découvrir mutuellement.</span><span class="sxs-lookup"><span data-stu-id="f3702-104">The Peer Name Resolution Protocol (PNRP) Namespace Provider (NSP) is a serverless name resolution technology that allows nodes to discover each other.</span></span> <span data-ttu-id="f3702-105">PNRP utilise l’API du fournisseur d’espace de noms Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="f3702-105">PNRP uses the Winsock 2 Namespace Provider API.</span></span>

<span data-ttu-id="f3702-106">La prise en charge D’ipv6 est requise par PNRP et est le seul protocole Internet natif à l’API.</span><span class="sxs-lookup"><span data-stu-id="f3702-106">IPv6 support is required by PNRP and is the only Internet Protocol native to the API.</span></span> <span data-ttu-id="f3702-107">Toutefois, PNRP peut résoudre les adresses IPv4 via les technologies de transition 6to4 ou [Teredo](/windows/desktop/Teredo/portal) .</span><span class="sxs-lookup"><span data-stu-id="f3702-107">However, PNRP can resolve IPv4 addresses via the 6to4 or [Teredo](/windows/desktop/Teredo/portal) transition technologies.</span></span> <span data-ttu-id="f3702-108">Les utilisateurs de Windows XP avec Service Pack 1 (SP1) doivent télécharger le [Pack de mise en réseau avancée](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) pour activer la prise en charge IPv6 requise par PNRP.</span><span class="sxs-lookup"><span data-stu-id="f3702-108">Windows XP with Service Pack 1 (SP1) users must download the [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) to enable the IPv6 support required by PNRP.</span></span>

> [!Note]  
> <span data-ttu-id="f3702-109">Les applications utilisant PNRP dans un environnement avec un pare-feu nécessitent des groupes d’exceptions qui couvrent le port propre à l’application, ainsi que le port « 3540-UDP » pour PNRP.</span><span class="sxs-lookup"><span data-stu-id="f3702-109">Applications using PNRP in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="f3702-110">Ces groupes d’exceptions doivent être activés chaque fois que l’application est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f3702-110">These exception groups should be enabled whenever the application is running.</span></span>

 

<span data-ttu-id="f3702-111">Alors que le protocole PNRP 2,0 est natif pour les plateformes Windows Vista et Windows Server 2008, les utilisateurs de Windows XP doivent télécharger Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) pour effectuer une mise à niveau vers PNRP 2,0.</span><span class="sxs-lookup"><span data-stu-id="f3702-111">While PNRP 2.0 is native to the Windows Vista and Windows Server 2008 platforms, Windows XP users must download Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) to upgrade to PNRP 2.0.</span></span>

 

 
