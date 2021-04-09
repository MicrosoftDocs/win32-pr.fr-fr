---
description: Il est important de s’assurer que les nouvelles applications Winsock et les applications existantes sont entièrement compatibles avec IPv6.
ms.assetid: 48aa6be8-e8a2-48a5-aa71-3e5ed7032551
title: Protocole Internet version 6 (IPv6)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9647b70571b0bc81cbea508cf2e3bb55662efdf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862565"
---
# <a name="internet-protocol-version-6-ipv6"></a><span data-ttu-id="4acb8-103">Protocole Internet version 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="4acb8-103">Internet Protocol Version 6 (IPv6)</span></span>

<span data-ttu-id="4acb8-104">Il est important de s’assurer que les nouvelles applications Winsock et les applications existantes sont entièrement compatibles avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="4acb8-104">It is important to ensure that new Winsock applications as well as existing applications are fully compatible with IPv6.</span></span> <span data-ttu-id="4acb8-105">La disponibilité de l’espace d’adressage IPv4 pour les nouvelles allocations d’adresses IPv4 était épuisée pour l’Asie et le Pacifique dans 2011.</span><span class="sxs-lookup"><span data-stu-id="4acb8-105">The availability of the IPv4 address space for new IPv4 address allocations was exhausted for Asia and the Pacific in 2011.</span></span> <span data-ttu-id="4acb8-106">D’autres parties du monde devraient être épuisées dans quelques années.</span><span class="sxs-lookup"><span data-stu-id="4acb8-106">Other parts of the world are expected to be exhausted in a few years.</span></span>

<span data-ttu-id="4acb8-107">Un pourcentage croissant de nouveaux sites Web et services est disponible à l’aide d’adresses IPv6.</span><span class="sxs-lookup"><span data-stu-id="4acb8-107">A growing percentage of new websites and services are available using IPv6 addresses.</span></span> <span data-ttu-id="4acb8-108">De nombreux utilisateurs Internet sur les marchés émergents dépendent de IPv6 pour l’accès à Internet.</span><span class="sxs-lookup"><span data-stu-id="4acb8-108">Many Internet users in emerging markets are dependent on IPv6 for Internet access.</span></span>

<span data-ttu-id="4acb8-109">Microsoft s’engage à prendre en charge IPv6 de longue durée.</span><span class="sxs-lookup"><span data-stu-id="4acb8-109">Microsoft has a long commitment of supporting IPv6.</span></span> <span data-ttu-id="4acb8-110">La prise en charge complète d’IPv6 est fournie sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4acb8-110">Full IPv6 support is provided on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="4acb8-111">Ce document fournit des informations sur la prise en charge de Winsock pour IPv6 :</span><span class="sxs-lookup"><span data-stu-id="4acb8-111">This document provides information about the Winsock support for IPv6:</span></span>

-   [<span data-ttu-id="4acb8-112">Utilisation d'une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="4acb8-112">Using IPv6</span></span>](using-ipv6-2.md)
-   [<span data-ttu-id="4acb8-113">Utilisation d’Internet Explorer pour accéder aux sites Web IPv6</span><span class="sxs-lookup"><span data-stu-id="4acb8-113">Using Internet Explorer to Access IPv6 Websites</span></span>](using-internet-explorer-to-access-ipv6-web-sites-2.md)
-   [<span data-ttu-id="4acb8-114">Configurations recommandées pour IPv6</span><span class="sxs-lookup"><span data-stu-id="4acb8-114">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
-   [<span data-ttu-id="4acb8-115">Autres rubriques IPv6</span><span class="sxs-lookup"><span data-stu-id="4acb8-115">Additional IPv6 Topics</span></span>](additional-topics-2.md)

<span data-ttu-id="4acb8-116">Pour plus d’informations sur l’ajout de la fonctionnalité IPv6 à vos applications Windows Sockets, consultez le [Guide IPv6 pour les applications Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="4acb8-116">For additional information on adding IPv6 capability to your Windows Sockets applications, see [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

<span data-ttu-id="4acb8-117">Une introduction au protocole IPv6 ainsi que des vues d’ensemble sur le déploiement et les technologies de transition IPv6 sont disponibles sur TechNet au niveau de [Microsoft Internet Protocol version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4acb8-117">An introduction to the IPv6 protocol along with overviews on deployment and IPv6 transitioning technologies is available on Technet at [Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4acb8-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4acb8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4acb8-119">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="4acb8-119">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="4acb8-120">Prise en charge D’ipv6</span><span class="sxs-lookup"><span data-stu-id="4acb8-120">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="4acb8-121">Version préliminaire de la technologie IPv6 pour Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4acb8-121">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

<span data-ttu-id="4acb8-122">[Protocole Microsoft Internet Protocol version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4acb8-122">[Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span></span>
</dt> </dl>

 

 
