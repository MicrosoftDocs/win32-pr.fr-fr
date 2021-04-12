---
description: Les tables du groupe procédure d’installation contrôlent les tâches effectuées lors de l’installation par actions standard et actions personnalisées.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Groupe de tables de procédure d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320878"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="f3f6d-103">Groupe de tables de procédure d’installation</span><span class="sxs-lookup"><span data-stu-id="f3f6d-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="f3f6d-104">Les tables du groupe procédure d’installation contrôlent les tâches effectuées lors de l’installation par [actions standard](standard-actions.md) et [actions personnalisées](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f3f6d-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="f3f6d-105">Certaines des tables de ce groupe contrôlent une action de haut niveau en fournissant une séquence d’actions.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="f3f6d-106">Chacune des tables de séquences suivantes contrôle une partie d’une action de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="f3f6d-107">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="f3f6d-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="f3f6d-108">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f3f6d-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="f3f6d-109">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="f3f6d-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="f3f6d-110">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f3f6d-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="f3f6d-111">Table AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="f3f6d-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="f3f6d-112">Table AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="f3f6d-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="f3f6d-113">Il peut y avoir des situations dans lesquelles une installation doit effectuer une opération qui n’est pas possible en utilisant uniquement des [actions standard](standard-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f3f6d-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="f3f6d-114">Pour offrir le plus grand degré de flexibilité, le programme d’installation fournit aux auteurs d’installation la possibilité de créer leurs propres actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="f3f6d-115">Si vous avez des actions personnalisées, vous devez les inscrire auprès du programme d’installation en remplissant la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="f3f6d-116">La [table CustomAction](customaction-table.md) fournit les moyens d’intégrer du code personnalisé et des données dans le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="f3f6d-117">Le code exécuté peut être un flux contenu dans la base de données, un fichier récemment installé ou un exécutable existant.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="f3f6d-118">Les tableaux suivants étendent les fonctionnalités du programme d’installation pour manipuler les fichiers et les dossiers lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="f3f6d-119">La [table RemoveFile](removefile-table.md) contient la liste des fichiers qui sont supprimés au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="f3f6d-120">La [table RemoveIniFile](removeinifile-table.md) contient les informations dont une application a besoin pour supprimer des fichiers. ini.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="f3f6d-121">La [table RemoveRegistry](removeregistry-table.md) contient les informations qui sont supprimées du Registre système lorsque le composant correspondant est sélectionné pour être installé.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="f3f6d-122">Le [tableau CreateFolder](createfolder-table.md) répertorie les dossiers qui doivent être créés pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="f3f6d-123">Bien que le programme d’installation crée des dossiers lorsqu’ils sont nécessaires, ceux-ci sont supprimés dès qu’ils sont vides.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="f3f6d-124">La liste des dossiers dans la table CreateFolder n’est pas supprimée tant que le composant n’est pas désinstallé.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="f3f6d-125">La [table MoveFile](movefile-table.md) contient une liste de fichiers à déplacer ou à copier à partir d’un répertoire source spécifié sur l’ordinateur de l’utilisateur vers un répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="f3f6d-126">Il n’est pas nécessaire d’utiliser la table MoveFile pour décrire les fichiers associés aux composants que vous installez.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="f3f6d-127">Pour définir les conditions requises qui doivent être remplies pour lancer l’installation, remplissez la table LaunchCondition.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="f3f6d-128">La [table LaunchCondition](launchcondition-table.md) contient une liste de conditions, qui doivent toutes être satisfaites pour que l’action aboutisse.</span><span class="sxs-lookup"><span data-stu-id="f3f6d-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 



