---
title: Comment sécuriser mon serveur RPC maintenant
description: L’utilisation de la sécurité décrite dans cette section, fournie ailleurs dans le kit de développement logiciel (SDK) RPC et généralement acceptée comme des pratiques de sécurité appropriées, aboutit à un serveur qui est très sécurisé. Ces serveurs sont protégés contre les attaques par pénétration ou les violations de confidentialité.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940015"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="42c12-104">Quelle est la sécurité de mon serveur RPC maintenant ?</span><span class="sxs-lookup"><span data-stu-id="42c12-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="42c12-105">L’utilisation de la sécurité décrite dans cette section, fournie ailleurs dans le kit de développement logiciel (SDK) RPC et généralement acceptée comme des pratiques de sécurité appropriées, aboutit à un serveur qui est très sécurisé.</span><span class="sxs-lookup"><span data-stu-id="42c12-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="42c12-106">Ces serveurs sont protégés contre les attaques par pénétration ou les violations de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="42c12-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="42c12-107">Si l’État est conservé entre les appels RPC, assurez-vous qu’un client unique n’entraîne pas l’allocation de ressources excessives, ce qui pourrait potentiellement refuser le service à d’autres clients.</span><span class="sxs-lookup"><span data-stu-id="42c12-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




