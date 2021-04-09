---
title: Développement et déploiement sur le réseau
description: La plupart des développeurs écrivent et testent leurs logiciels sur un réseau local fiable et rapide.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029086"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="1602f-103">Développement et déploiement sur le réseau</span><span class="sxs-lookup"><span data-stu-id="1602f-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="1602f-104">La plupart des développeurs écrivent et testent leurs logiciels sur un réseau local fiable et rapide.</span><span class="sxs-lookup"><span data-stu-id="1602f-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="1602f-105">Le client et le serveur sont souvent sur le même segment de réseau.</span><span class="sxs-lookup"><span data-stu-id="1602f-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="1602f-106">Dans ce cas, le réseau ne répond rarement pas et la connectivité est rarement perdue.</span><span class="sxs-lookup"><span data-stu-id="1602f-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="1602f-107">En cas de déploiement dans un environnement client, toutefois, le client et le serveur sont souvent sur différents segments du réseau, éventuellement à distance géographique, et le serveur est très chargé avec d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="1602f-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="1602f-108">En d’autres termes : la réactivité du réseau ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1602f-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="1602f-109">Cet article explique comment créer des architectures client/serveur robustes face à l’incertitude introduite par un réseau intrinsèquement fiable et des serveurs potentiellement indisponibles.</span><span class="sxs-lookup"><span data-stu-id="1602f-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




