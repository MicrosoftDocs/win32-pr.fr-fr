---
title: Sécurité et informations d’erreur étendues
description: Les informations d’erreur étendues offrent des données très utiles lors de la résolution d’un problème RPC, mais ces données sont souvent considérées comme confidentielles par les organisations soucieuses de la sécurité.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675234"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="67fa1-103">Sécurité et informations d’erreur étendues</span><span class="sxs-lookup"><span data-stu-id="67fa1-103">Security and Extended Error Information</span></span>

<span data-ttu-id="67fa1-104">Les informations d’erreur étendues offrent des données très utiles lors de la résolution d’un problème RPC, mais ces données sont souvent considérées comme confidentielles par les organisations soucieuses de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="67fa1-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="67fa1-105">En considération de tels problèmes de sécurité, les informations d’erreur étendues sont désactivées par défaut.</span><span class="sxs-lookup"><span data-stu-id="67fa1-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="67fa1-106">Les informations d’erreur étendues sont toujours générées lorsque les informations d’erreur étendues sont désactivées, mais les informations ne sont jamais transmises au-delà des limites des processus ou des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="67fa1-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="67fa1-107">Cette approche permet d’utiliser les informations d’erreur par les outils qui ont accès à l’espace d’adressage du processus, tels que les débogueurs.</span><span class="sxs-lookup"><span data-stu-id="67fa1-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="67fa1-108">Lorsqu’elles sont activées, les informations d’erreur étendues sont générées et peuvent être envoyées entre les limites du processus et de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="67fa1-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="67fa1-109">Actuellement, les informations d’erreur étendues sont utilisées pour les séquences de protocole orientées connexion et les appels RPC locaux (LRPC).</span><span class="sxs-lookup"><span data-stu-id="67fa1-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="67fa1-110">Elle est partiellement implémentée pour les datagrammes.</span><span class="sxs-lookup"><span data-stu-id="67fa1-110">It is partially implemented for datagrams.</span></span>

 

 




