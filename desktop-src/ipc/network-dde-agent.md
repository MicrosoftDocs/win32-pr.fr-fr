---
description: L’agent DDE réseau démarre le DDE réseau s’il détecte une activité DDE de réseau local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agent DDE réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516820"
---
# <a name="network-dde-agent"></a><span data-ttu-id="80245-103">Agent DDE réseau</span><span class="sxs-lookup"><span data-stu-id="80245-103">Network DDE Agent</span></span>

<span data-ttu-id="80245-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="80245-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="80245-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="80245-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="80245-106">L’agent DDE réseau démarre le DDE réseau s’il détecte une activité DDE de réseau local.</span><span class="sxs-lookup"><span data-stu-id="80245-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="80245-107">Il ne détecte pas un client distant tentant de se connecter.</span><span class="sxs-lookup"><span data-stu-id="80245-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="80245-108">Par conséquent, avant qu’un client puisse se connecter, DDE réseau doit être démarré sur l’ordinateur serveur.</span><span class="sxs-lookup"><span data-stu-id="80245-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="80245-109">Notez que le DDE réseau n’est pas démarré par défaut.</span><span class="sxs-lookup"><span data-stu-id="80245-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="80245-110">Pour démarrer le DDE réseau, exécutez NETDDE.EXE.</span><span class="sxs-lookup"><span data-stu-id="80245-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="80245-111">Ce fichier se trouve dans votre répertoire Windows.</span><span class="sxs-lookup"><span data-stu-id="80245-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="80245-112">L’agent DDE réseau démarre également les applications nécessaires pour DDE réseau.</span><span class="sxs-lookup"><span data-stu-id="80245-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="80245-113">Une fois le DDE réseau démarré, les conversations DDE sont contrôlées via une fenêtre DDE réseau associée à l’une des applications DDE réseau.</span><span class="sxs-lookup"><span data-stu-id="80245-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="80245-114">Cette application agit comme un proxy.</span><span class="sxs-lookup"><span data-stu-id="80245-114">This application acts as a proxy.</span></span> <span data-ttu-id="80245-115">Il communique avec toutes les applications DDE locales et distantes.</span><span class="sxs-lookup"><span data-stu-id="80245-115">It communicates with all local and remote DDE applications.</span></span>

 

 



