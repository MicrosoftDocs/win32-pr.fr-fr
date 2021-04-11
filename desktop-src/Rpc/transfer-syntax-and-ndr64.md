---
title: Syntaxe de transfert et NDR64
description: Le protocole câble NDR, également appelé syntaxe de transfert, permet aux appels RPC de traverser le réseau.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031277"
---
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="d7ceb-103">Syntaxe de transfert et NDR64</span><span class="sxs-lookup"><span data-stu-id="d7ceb-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="d7ceb-104">Le protocole câble NDR, également appelé syntaxe de transfert, permet aux appels RPC de traverser le réseau.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="d7ceb-105">Le protocole Wire définit la représentation filaire d’un appel RPC, telle que l’ordre dans lequel les membres de données sont marshalés, l’alignement des données sur le câble, les informations supplémentaires incluses dans les données et d’autres problèmes.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="d7ceb-106">Le protocole NDR64 est une extension de la syntaxe de transfert de rapport de remise 32 bits, créée spécifiquement pour permettre aux développeurs ciblant des systèmes 64 bits d’obtenir des performances optimisées.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="d7ceb-107">Les différences entre le format de transmission de NDR et le format de câble NDR64 traitent la taille différente des pointeurs dans un environnement 64 bits, ainsi que d’autres problèmes.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="d7ceb-108">Le mécanisme de NDR64 est géré par RPC.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="d7ceb-109">Les développeurs doivent uniquement utiliser le commutateur de ligne de commande/[**protocole**](/windows/desktop/Midl/-protocol)**tout** MIDL pour bénéficier des avantages de NDR64 sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="d7ceb-110">NDR64 est disponible uniquement sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d7ceb-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 