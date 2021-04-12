---
description: Résolution de noms indépendante du protocole et Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Résolution de noms Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318366"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="469c2-103">Résolution de noms Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="469c2-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="469c2-104">Lors du développement d’une application client/serveur indépendante du protocole, deux exigences de base existent en ce qui concerne la résolution de noms et l’inscription :</span><span class="sxs-lookup"><span data-stu-id="469c2-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="469c2-105">La capacité du serveur de l’application (service) à inscrire son existence dans (ou à être accessible) à un ou plusieurs espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="469c2-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="469c2-106">Capacité de l’application cliente à rechercher le service dans un espace de noms et à obtenir le protocole de transport et les informations d’adressage requis.</span><span class="sxs-lookup"><span data-stu-id="469c2-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="469c2-107">Pour ceux qui sont habitués au développement d’applications basées sur TCP/IP, cela peut sembler un peu plus grand que la recherche d’une adresse d’hôte, puis l’utilisation d’un numéro de port convenu.</span><span class="sxs-lookup"><span data-stu-id="469c2-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="469c2-108">Toutefois, d’autres schémas de mise en réseau autorisent l’emplacement du service, le protocole utilisé pour le service et d’autres attributs à découvrir au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="469c2-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="469c2-109">Pour prendre en charge la grande diversité des fonctionnalités disponibles dans les services de noms existants, l’interface Windows Sockets 2 adopte le modèle décrit dans les rubriques de cette section.</span><span class="sxs-lookup"><span data-stu-id="469c2-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="469c2-110">Cette section décrit les fonctionnalités de résolution de noms indépendantes des protocoles disponibles pour les développeurs Winsock.</span><span class="sxs-lookup"><span data-stu-id="469c2-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="469c2-111">La liste suivante décrit les rubriques de cette section :</span><span class="sxs-lookup"><span data-stu-id="469c2-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="469c2-112">Modèle de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="469c2-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="469c2-113">Résumé des fonctions de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="469c2-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="469c2-114">Structures de données de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="469c2-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="469c2-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="469c2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="469c2-116">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="469c2-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



