---
description: La base de données du programme d’installation permet au développeur d’un package d’installation de contrôler le transfert d’une application d’une source à une image cible.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Utilisation de la base de données du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545818"
---
# <a name="using-the-installer-database"></a><span data-ttu-id="26e69-103">Utilisation de la base de données du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="26e69-103">Using the Installer Database</span></span>

<span data-ttu-id="26e69-104">La [base de données du programme](installer-database.md) d’installation permet au développeur d’un package d’installation de contrôler le transfert d’une application d’une source à une image cible.</span><span class="sxs-lookup"><span data-stu-id="26e69-104">The [Installer Database](installer-database.md) enables the developer of an installation package to control the transfer of an application from a source to a target image.</span></span> <span data-ttu-id="26e69-105">La disposition des images source et cible de l’application est spécifiée dans la table de [répertoires](directory-table.md) et les actions qui installent l’application sont spécifiées dans six tables de séquence :</span><span class="sxs-lookup"><span data-stu-id="26e69-105">The layout of both the source and target images of the application are specified in the [Directory](directory-table.md) table and the actions that install the application are specified in six sequence tables:</span></span>

-   <span data-ttu-id="26e69-106">Table [InstallUISequence](installuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="26e69-106">[InstallUISequence](installuisequence-table.md) table</span></span>
-   <span data-ttu-id="26e69-107">Table [InstallExecuteSequence](installexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="26e69-107">[InstallExecuteSequence](installexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="26e69-108">Table [AdminUISequence](adminuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="26e69-108">[AdminUISequence](adminuisequence-table.md) table</span></span>
-   <span data-ttu-id="26e69-109">Table [AdminExecuteSequence](adminexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="26e69-109">[AdminExecuteSequence](adminexecutesequence-table.md) table</span></span>
-   <span data-ttu-id="26e69-110">Table [AdvtUISequence](advtuisequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="26e69-110">[AdvtUISequence](advtuisequence-table.md) table</span></span>
-   <span data-ttu-id="26e69-111">Table [AdvtExecuteSequence](advtexecutesequence-table.md)</span><span class="sxs-lookup"><span data-stu-id="26e69-111">[AdvtExecuteSequence](advtexecutesequence-table.md) table</span></span>

<span data-ttu-id="26e69-112">Les sections suivantes décrivent l’utilisation [de la base de données du programme d’installation](installer-database.md):</span><span class="sxs-lookup"><span data-stu-id="26e69-112">The following sections describe how to use the [Installer Database](installer-database.md):</span></span>

-   [<span data-ttu-id="26e69-113">Utilisation de la table Directory</span><span class="sxs-lookup"><span data-stu-id="26e69-113">Using the Directory Table</span></span>](using-the-directory-table.md)
-   [<span data-ttu-id="26e69-114">Utilisation d’une table de séquences</span><span class="sxs-lookup"><span data-stu-id="26e69-114">Using a Sequence Table</span></span>](using-a-sequence-table.md)
-   [<span data-ttu-id="26e69-115">Obtention d’un descripteur de base de données</span><span class="sxs-lookup"><span data-stu-id="26e69-115">Obtaining a Database Handle</span></span>](obtaining-a-database-handle.md)
-   [<span data-ttu-id="26e69-116">Validation des bases de données</span><span class="sxs-lookup"><span data-stu-id="26e69-116">Committing Databases</span></span>](committing-databases.md)
-   [<span data-ttu-id="26e69-117">Importation et exportation</span><span class="sxs-lookup"><span data-stu-id="26e69-117">Importing and Exporting</span></span>](importing-and-exporting.md)
-   [<span data-ttu-id="26e69-118">Fusion de bases de données</span><span class="sxs-lookup"><span data-stu-id="26e69-118">Merging Databases</span></span>](merging-databases.md)
-   [<span data-ttu-id="26e69-119">Attribution d’un nom aux tables, propriétés et actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="26e69-119">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
-   [<span data-ttu-id="26e69-120">Limitations OLE sur les flux</span><span class="sxs-lookup"><span data-stu-id="26e69-120">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
-   [<span data-ttu-id="26e69-121">Utilisation des requêtes</span><span class="sxs-lookup"><span data-stu-id="26e69-121">Working with Queries</span></span>](working-with-queries.md)
-   [<span data-ttu-id="26e69-122">Ajout de données binaires à une table à l’aide de SQL</span><span class="sxs-lookup"><span data-stu-id="26e69-122">Adding Binary Data to a Table Using SQL</span></span>](adding-binary-data-to-a-table-using-sql.md)
-   [<span data-ttu-id="26e69-123">Utilisation des enregistrements</span><span class="sxs-lookup"><span data-stu-id="26e69-123">Working with Records</span></span>](working-with-records.md)
-   [<span data-ttu-id="26e69-124">Utilisation des emplacements de dossiers</span><span class="sxs-lookup"><span data-stu-id="26e69-124">Working with Folder Locations</span></span>](working-with-folder-locations.md)
-   [<span data-ttu-id="26e69-125">Spécification de l’ordre d’inscription automatique</span><span class="sxs-lookup"><span data-stu-id="26e69-125">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
-   [<span data-ttu-id="26e69-126">Mesures de conditionnement à exécuter pendant la suppression</span><span class="sxs-lookup"><span data-stu-id="26e69-126">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
-   [<span data-ttu-id="26e69-127">Appel de fonctions de base de données à partir de programmes</span><span class="sxs-lookup"><span data-stu-id="26e69-127">Calling Database Functions from Programs</span></span>](calling-database-functions-from-programs.md)
-   [<span data-ttu-id="26e69-128">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="26e69-128">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
-   [<span data-ttu-id="26e69-129">Format de définition de colonne</span><span class="sxs-lookup"><span data-stu-id="26e69-129">Column Definition Format</span></span>](column-definition-format.md)
-   [<span data-ttu-id="26e69-130">Déterminer si une colonne est une clé primaire ou externe</span><span class="sxs-lookup"><span data-stu-id="26e69-130">Determining Whether a Column is a Primary or External Key</span></span>](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



