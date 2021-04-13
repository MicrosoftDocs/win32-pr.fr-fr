---
description: Une diffusion générale via Internet est obtenue en définissant les \_ champs sa netnum et sa \_ nodeNum sur Binary (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Diffusion de tous les itinéraires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484961"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="eb803-103">Diffusion de tous les itinéraires</span><span class="sxs-lookup"><span data-stu-id="eb803-103">All Routes Broadcast</span></span>

<span data-ttu-id="eb803-104">Une diffusion générale via Internet est obtenue en définissant les champs **sa \_ netnum** et **sa \_ nodeNum** sur Binary (1).</span><span class="sxs-lookup"><span data-stu-id="eb803-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="eb803-105">Le fournisseur de services traduit cette requête en un paquet type-20, que les routeurs IPX reconnaissent et transfèrent.</span><span class="sxs-lookup"><span data-stu-id="eb803-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="eb803-106">Le paquet visite tous les sous-réseaux et peut être dupliqué plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="eb803-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="eb803-107">Les destinataires doivent gérer plusieurs copies dupliquées du datagramme.</span><span class="sxs-lookup"><span data-stu-id="eb803-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="eb803-108">L’utilisation de ce type de diffusion n’est pas populaire parmi les administrateurs réseau. son utilisation doit donc être extrêmement limitée.</span><span class="sxs-lookup"><span data-stu-id="eb803-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="eb803-109">De nombreux routeurs désactivent ce type de diffusion, laissant les parties du sous-réseau invisible au paquet.</span><span class="sxs-lookup"><span data-stu-id="eb803-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



