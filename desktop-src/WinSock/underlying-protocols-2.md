---
description: Certains protocoles dont votre application dépend pour certains services, tels que l’appel de procédure distante (RPC), peuvent avoir des fonctions et des structures dépendantes de la version IP qui nécessitent que vous modifiiez votre application en termes d’utilisation.
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: Protocoles sous-jacents pour les applications Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88789a5f4cd557111c6e1aee8c51ba00eed25e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201423"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a><span data-ttu-id="b463e-103">Protocoles sous-jacents pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="b463e-103">Underlying Protocols for IPv6 Winsock Applications</span></span>

<span data-ttu-id="b463e-104">Certains protocoles dont votre application dépend pour certains services, tels que l’appel de procédure distante (RPC), peuvent avoir des fonctions et des structures dépendantes de la version IP qui nécessitent que vous modifiiez votre application en termes d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b463e-104">Some protocols that your application depends on for certain services, such as Remote Procedure Call (RPC), may have IP-version dependent functions and structures that require you to modify your application in terms of their usage.</span></span>

<span data-ttu-id="b463e-105">Une partie du processus de modification de votre code pour prendre en charge IPv6 doit inclure la détermination de l’utilisation des protocoles sous-jacents (du point de vue de la pile, ces protocoles sont considérés comme des protocoles de couche supérieure) nécessitent une modification pour pouvoir utiliser correctement IPv6.</span><span class="sxs-lookup"><span data-stu-id="b463e-105">Part of the process to modify your code to support IPv6 should include determining whether the use of the underlying protocols (from the perspective of the stack, these protocols are considered higher-layer protocols) require modification in order to properly make use of IPv6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b463e-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b463e-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b463e-107">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b463e-107">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="b463e-108">Modification des structures de données pour IPv6 Winsock appications</span><span class="sxs-lookup"><span data-stu-id="b463e-108">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="b463e-109">Sockets à double pile pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="b463e-109">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="b463e-110">Appels de fonction pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="b463e-110">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="b463e-111">Utilisation d’adresses IPv4 codées en dur</span><span class="sxs-lookup"><span data-stu-id="b463e-111">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="b463e-112">Problèmes d’interface utilisateur pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="b463e-112">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> </dl>

 

 



