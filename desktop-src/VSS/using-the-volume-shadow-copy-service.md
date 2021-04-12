---
description: Les opérations de sauvegarde et de restauration VSS utilisent chacune un protocole pour l’interaction des systèmes qui utilisent le stockage de masse (Writers) et ceux qui les sauvegardent (demandeurs).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Utilisation de l’Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526302"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="3765e-103">Utilisation de l’Service VSS</span><span class="sxs-lookup"><span data-stu-id="3765e-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="3765e-104">Les opérations de sauvegarde et de restauration VSS utilisent chacune un protocole pour l’interaction des systèmes qui utilisent le stockage de masse (Writers) et ceux qui les sauvegardent (demandeurs).</span><span class="sxs-lookup"><span data-stu-id="3765e-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="3765e-105">Les opérations de sauvegarde et de restauration sont principalement pilotées par le demandeur, qui contrôle le comportement de l’enregistreur et du fournisseur en générant des événements COM à l’échelle du writer à traiter.</span><span class="sxs-lookup"><span data-stu-id="3765e-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="3765e-106">Étant donné que les méthodes de génération d’événements sont asynchrones, les Writers ont un contrôle limité de l’état du demandeur via les gestionnaires asynchrones disponibles pour VSS (voir [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span><span class="sxs-lookup"><span data-stu-id="3765e-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="3765e-107">Cette interaction requiert des structures de données de base décrivant les fichiers et les groupes de fichiers ([*composants*](vssgloss-c.md)), ainsi qu’un modèle de métadonnées permettant de stocker les informations de sauvegarde et d’autoriser la communication de rédacteur/demandeur.</span><span class="sxs-lookup"><span data-stu-id="3765e-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="3765e-108">Compatibilité des applications VSS</span><span class="sxs-lookup"><span data-stu-id="3765e-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="3765e-109">Configuration de VSS</span><span class="sxs-lookup"><span data-stu-id="3765e-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="3765e-110">Métadonnées VSS</span><span class="sxs-lookup"><span data-stu-id="3765e-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="3765e-111">Utilisation de la sélectivité et des chemins logiques</span><span class="sxs-lookup"><span data-stu-id="3765e-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="3765e-112">Vue d’ensemble du traitement d’une sauvegarde sous VSS</span><span class="sxs-lookup"><span data-stu-id="3765e-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="3765e-113">Vue d’ensemble du traitement d’une restauration sous VSS</span><span class="sxs-lookup"><span data-stu-id="3765e-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



