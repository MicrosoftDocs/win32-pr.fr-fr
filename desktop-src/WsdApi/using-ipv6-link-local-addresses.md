---
description: L’adressage local de la liaison IPv6 dans les messages SOAP fournit un défi unique, car les adresses IPv6 à liaison locale nécessitent un ID d’étendue explicite, mais l’ID d’étendue n’a que la signification de l’ordinateur local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Utilisation d’adresses lien-local IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114274"
---
# <a name="using-ipv6-link-local-addresses"></a><span data-ttu-id="13cd6-103">Utilisation d’adresses lien-local IPv6</span><span class="sxs-lookup"><span data-stu-id="13cd6-103">Using IPv6 Link-Local Addresses</span></span>

<span data-ttu-id="13cd6-104">L’adressage local de la liaison IPv6 dans les messages SOAP fournit un défi unique, car les adresses IPv6 à liaison locale nécessitent un ID d’étendue explicite, mais l’ID d’étendue n’a que la signification de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="13cd6-104">IPv6 link-local addressing in SOAP messages provides a unique challenge, as IPv6 link-local addresses require a scope ID to be meaningful, but the scope ID only has meaning for the local machine.</span></span> <span data-ttu-id="13cd6-105">Toutes les implémentations de clients et d’appareils doivent supprimer l’ID d’étendue avant d’envoyer une adresse lien-local IPv6 dans un message SOAP.</span><span class="sxs-lookup"><span data-stu-id="13cd6-105">All client and device implementations must remove the scope ID before sending an IPv6 link-local address in a SOAP message.</span></span> <span data-ttu-id="13cd6-106">En outre, lorsqu’une adresse de lien local IPv6 est reçue dans un message, l’interface sur laquelle le message a été reçu doit être connue afin que l’adresse locale de lien complète avec l’ID d’étendue puisse être reconstruite.</span><span class="sxs-lookup"><span data-stu-id="13cd6-106">Additionally, when an IPv6 link-local address is received in a message, the interface the message was received on must be known so the complete link local address with scope ID can be reconstructed.</span></span>

 

 



