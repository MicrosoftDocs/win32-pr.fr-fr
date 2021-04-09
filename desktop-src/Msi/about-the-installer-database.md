---
description: La base de données Windows Installer se compose de nombreuses tables liées entre elles qui forment une base de données relationnelle des informations nécessaires à l’installation d’un groupe d’applications.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: À propos de la base de données du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864534"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="c064a-103">À propos de la base de données du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="c064a-103">About the Installer Database</span></span>

<span data-ttu-id="c064a-104">La base de données Windows Installer se compose de nombreuses tables liées entre elles qui forment une base de données relationnelle des informations nécessaires à l’installation d’un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="c064a-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="c064a-105">Étant donné que la base de données est relationnelle, les tables sont liées par les données dans les valeurs de clé primaire et étrangère.</span><span class="sxs-lookup"><span data-stu-id="c064a-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="c064a-106">Cela constitue une méthode efficace pour modifier le processus d’installation et signifie que les utilisateurs peuvent personnaliser plus facilement une application ou un groupe d’applications de grande taille.</span><span class="sxs-lookup"><span data-stu-id="c064a-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="c064a-107">Les tables de base de données reflètent la disposition générale du groupe entier d’applications, notamment :</span><span class="sxs-lookup"><span data-stu-id="c064a-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="c064a-108">Fonctionnalités disponibles</span><span class="sxs-lookup"><span data-stu-id="c064a-108">Available features</span></span>
-   <span data-ttu-id="c064a-109">Composants</span><span class="sxs-lookup"><span data-stu-id="c064a-109">Components</span></span>
-   <span data-ttu-id="c064a-110">Relation entre les fonctionnalités et les composants</span><span class="sxs-lookup"><span data-stu-id="c064a-110">Relationship between features and components</span></span>
-   <span data-ttu-id="c064a-111">Paramètres du Registre nécessaires</span><span class="sxs-lookup"><span data-stu-id="c064a-111">Necessary registry settings</span></span>
-   <span data-ttu-id="c064a-112">Interface utilisateur pour l’application</span><span class="sxs-lookup"><span data-stu-id="c064a-112">User interface for the application</span></span>

<span data-ttu-id="c064a-113">Pour créer une base de données d’installation, vous devez remplir les tables avec toutes les informations relatives aux applications et au processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="c064a-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="c064a-114">La création manuelle de toutes ces tables devient une tâche importante, même pour une installation de taille modérée. par conséquent, certains outils tiers sont disponibles pour faciliter la création de la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="c064a-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="c064a-115">Les sections suivantes décrivent les groupes de tables de base de données associées.</span><span class="sxs-lookup"><span data-stu-id="c064a-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="c064a-116">Groupe de tables principales</span><span class="sxs-lookup"><span data-stu-id="c064a-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="c064a-117">Groupe de tables de fichiers</span><span class="sxs-lookup"><span data-stu-id="c064a-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="c064a-118">Groupe de tables de Registre</span><span class="sxs-lookup"><span data-stu-id="c064a-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="c064a-119">Groupe de tables système</span><span class="sxs-lookup"><span data-stu-id="c064a-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="c064a-120">Groupe de tables de localisateur</span><span class="sxs-lookup"><span data-stu-id="c064a-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="c064a-121">Groupe de tables d’informations sur les programmes</span><span class="sxs-lookup"><span data-stu-id="c064a-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="c064a-122">Groupe de tables de procédure d’installation</span><span class="sxs-lookup"><span data-stu-id="c064a-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="c064a-123">Légende du diagramme des relations d’entités</span><span class="sxs-lookup"><span data-stu-id="c064a-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="c064a-124">Fichiers d’archive de texte</span><span class="sxs-lookup"><span data-stu-id="c064a-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="c064a-125">Pour obtenir la liste complète de toutes les tables d’une base de données d’installation, consultez [tables de base de données](database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c064a-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c064a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c064a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c064a-127">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="c064a-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



