---
description: Les deux descripteurs (ou plus) qui font référence à un socket partagé peuvent être utilisés indépendamment en ce qui concerne les e/s.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Directives de précédence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113022"
---
# <a name="precedence-guidelines"></a><span data-ttu-id="21518-103">Directives de précédence</span><span class="sxs-lookup"><span data-stu-id="21518-103">Precedence Guidelines</span></span>

<span data-ttu-id="21518-104">Les deux descripteurs (ou plus) qui font référence à un socket partagé peuvent être utilisés indépendamment en ce qui concerne les e/s.</span><span class="sxs-lookup"><span data-stu-id="21518-104">The two (or more) descriptors that reference a shared socket may be used independently as far as I/O is concerned.</span></span> <span data-ttu-id="21518-105">Toutefois, l’interface Windows Sockets n’implémente aucun type de contrôle d’accès, c’est pourquoi il revient aux processus impliqués à coordonner leurs opérations sur un socket partagé.</span><span class="sxs-lookup"><span data-stu-id="21518-105">However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket.</span></span> <span data-ttu-id="21518-106">Une utilisation courante pour les sockets partagés consiste à avoir un processus qui est responsable de la création de sockets et de l’établissement de connexions entre les sockets et les autres processus qui sont responsables de l’échange d’informations.</span><span class="sxs-lookup"><span data-stu-id="21518-106">A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections hand off sockets to other processes that are responsible for information exchange.</span></span>

<span data-ttu-id="21518-107">La règle générale pour la prise en charge de plusieurs opérations en attente sur des sockets partagés est qu’un fournisseur de services est encouragé à respecter toutes les opérations simultanées sur les sockets partagés, en particulier l’opération la plus récente sur un objet Socket.</span><span class="sxs-lookup"><span data-stu-id="21518-107">The general guideline for supporting multiple outstanding operations on shared sockets is that a service provider is encouraged to honor all simultaneous operations on shared sockets, especially the most recent operation on a socket object.</span></span> <span data-ttu-id="21518-108">Si nécessaire, cela peut se produire au détriment d’une partie des opérations précédentes, mais toujours en attente, qui retourneront WSAEINTR dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="21518-108">If need be, this may occur at the expense of canceling some of the previous but still pending operations, which will return WSAEINTR in this case.</span></span>

 

 



