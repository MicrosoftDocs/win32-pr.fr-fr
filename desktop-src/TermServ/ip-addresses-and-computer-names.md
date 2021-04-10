---
title: Adresses IP et noms d’ordinateurs
description: Il est déconseillé de supposer que le nom d’ordinateur ou l’ adresse IP affectée à l’ordinateur sont associés à un seul utilisateur, étant donné que plusieurs utilisateurs peuvent être connectés simultanément à un serveur hôte de Session Bureau à distance.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316194"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="131e5-103">Adresses IP et noms d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="131e5-103">IP addresses and computer names</span></span>

<span data-ttu-id="131e5-104">Plusieurs utilisateurs peuvent être connectés simultanément à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="131e5-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="131e5-105">Par conséquent, il n’est pas possible de supposer que le nom de l’ordinateur ou l’adresse IP affectée à l’ordinateur sont associés à un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="131e5-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="131e5-106">Cela diffère d’un environnement Windows à utilisateur unique, dans lequel un seul utilisateur est connecté à la fois.</span><span class="sxs-lookup"><span data-stu-id="131e5-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="131e5-107">Les applications qui utilisent le nom d’ordinateur ou l’adresse IP pour la licence ou comme moyen d’identifier une itération de l’application sur le réseau ne fonctionneront pas correctement dans un environnement Services Bureau à distance, car le nom d’ordinateur ou l’adresse IP du serveur peut être associé à de nombreux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="131e5-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="131e5-108">Dans un environnement de Services Bureau à distance, chaque terminal client ou émulateur de terminal possède une adresse IP et un nom d’ordinateur distincts.</span><span class="sxs-lookup"><span data-stu-id="131e5-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="131e5-109">Pour récupérer l’adresse IP et le nom d’ordinateur d’un client, appelez la fonction [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="131e5-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="131e5-110">Les autres fonctions qui récupèrent ces adresses réseau et noms d’ordinateurs récupèrent le nom et l’adresse du serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="131e5-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="131e5-111">Par exemple, la fonction [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) retourne le nom d’ordinateur du serveur.</span><span class="sxs-lookup"><span data-stu-id="131e5-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 