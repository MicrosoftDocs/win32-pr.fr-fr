---
description: 'En savoir plus sur : à propos du moteur de stockage extensible'
title: À propos du moteur de stockage extensible
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950914"
---
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="e7089-103">À propos du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="e7089-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="e7089-104">_**S’applique à :** Exchange Server 2013 | Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e7089-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="e7089-105">À propos du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="e7089-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="e7089-106">Le moteur ESE (Extensible Storage Engine) est un moteur de base de données qui stocke les informations dans une séquence logique.</span><span class="sxs-lookup"><span data-stu-id="e7089-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="e7089-107">Les informations peuvent être récupérées de manière séquentielle ou en accédant à des index définis.</span><span class="sxs-lookup"><span data-stu-id="e7089-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="e7089-108">Les mises à jour de la base de données sont implémentées avec une transaction afin de garantir des opérations sécurisées.</span><span class="sxs-lookup"><span data-stu-id="e7089-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="e7089-109">Le moteur ESE permet un accès simultané à plusieurs bases de données, notamment des bases de données de fichiers journaux de transactions qui peuvent être utilisées pour la récupération du système.</span><span class="sxs-lookup"><span data-stu-id="e7089-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="e7089-110">ESE est évolutif pour des applications volumineuses ou de petite taille.</span><span class="sxs-lookup"><span data-stu-id="e7089-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="e7089-111">Les fonctionnalités suivantes sont disponibles avec l’interface de programmation d’applications (API) ESE :</span><span class="sxs-lookup"><span data-stu-id="e7089-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="e7089-112">Sauvegarde et restauration : une application peut créer des copies cohérentes de l’état des données pendant qu’elle est en ligne et modifie activement l’état des données.</span><span class="sxs-lookup"><span data-stu-id="e7089-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="e7089-113">Navigation dans les curseurs : l’application peut naviguer avec le curseur pour accéder aux données de manière séquentielle ou à l’aide d’index.</span><span class="sxs-lookup"><span data-stu-id="e7089-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="e7089-114">Base de données : collection de tables qui sont sauvegardées et restaurées en tant qu’unité unique.</span><span class="sxs-lookup"><span data-stu-id="e7089-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="e7089-115">Journalisation et récupération après incident : l’API ESE garantit que la cohérence des données définie par l’application est honorée même en cas de panne du système.</span><span class="sxs-lookup"><span data-stu-id="e7089-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="e7089-116">Tables : structure fondamentale de la base de données ESE utilisée pour stocker les données.</span><span class="sxs-lookup"><span data-stu-id="e7089-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="e7089-117">Transaction : le moteur de base de données ESE fournit des transactions (ACID) durables isolées cohérentes atomiques qui permettent aux applications de récupérer des données uniquement à partir d’États de données fiables et gèrent la cohérence des données en cas d’arrêt inattendu du processus ou d’arrêt du système.</span><span class="sxs-lookup"><span data-stu-id="e7089-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="e7089-118">Scalable : l’application peut créer des bases de données aussi volumineuses que 100 Go ou une taille de 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="e7089-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

