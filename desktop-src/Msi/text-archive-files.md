---
description: Les tables de base de données Windows Installer peuvent être exportées vers des fichiers texte ASCII à l’aide de MsiDatabaseExport ou de la méthode d’exportation de l’objet de base de données.
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: Fichiers d’archive de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865745"
---
# <a name="text-archive-files"></a><span data-ttu-id="e07bf-103">Fichiers d’archive de texte</span><span class="sxs-lookup"><span data-stu-id="e07bf-103">Text Archive Files</span></span>

<span data-ttu-id="e07bf-104">Les tables de base de données Windows Installer peuvent être exportées vers des fichiers texte ASCII à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) ou de la méthode d' [**exportation**](database-export.md) de l’objet [**de base de données**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e07bf-104">The Windows Installer database tables can be exported to ASCII text files by using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) or the [**Export**](database-export.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="e07bf-105">Les informations contenues dans ces fichiers d’archive de texte peuvent ensuite être réimportées dans une base de données Windows Installer à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) ou de la méthode d' [importation](database-import.md) de l’objet **de base de données** .</span><span class="sxs-lookup"><span data-stu-id="e07bf-105">The information in these text archive files can then be imported back into a Windows Installer database using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the **Database** object.</span></span>

<span data-ttu-id="e07bf-106">Les outils tels que les [msidb.exe](msidb-exe.md) sont en mesure d’exporter et d’importer des fichiers d’archive de texte.</span><span class="sxs-lookup"><span data-stu-id="e07bf-106">Tools such as [msidb.exe](msidb-exe.md) are capable of exporting and importing text archive files.</span></span> <span data-ttu-id="e07bf-107">Consultez [Exporter](export-files.md) des fichiers et [importer des fichiers](import-files.md) pour obtenir des exemples de [script Windows Installer](windows-installer-scripting-examples.md) qui peuvent exporter et importer des fichiers d’archive de texte à partir d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="e07bf-107">See [Export Files](export-files.md) and [Import Files](import-files.md) for [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) that can export and import text archive files from a database.</span></span>

> [!Note]  
> <span data-ttu-id="e07bf-108">Les fichiers d’archive de texte ne sont pas destinés à modifier la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="e07bf-108">Text archive files are not intended as a means to edit the installation database.</span></span> <span data-ttu-id="e07bf-109">Pour créer et modifier un package d’installation, vous devez utiliser un outil de modification de table Windows Installer, tel qu' [Orca](orca-exe.md) ou un outil tiers.</span><span class="sxs-lookup"><span data-stu-id="e07bf-109">You should use a Windows Installer table editing tool, such as [Orca](orca-exe.md) or a third-party tool, to create and modify an installation package.</span></span>

 

<span data-ttu-id="e07bf-110">Les fichiers d’archive de texte peuvent être utilisés dans les cas suivants.</span><span class="sxs-lookup"><span data-stu-id="e07bf-110">Text archive files can be used for the following purposes.</span></span>

-   <span data-ttu-id="e07bf-111">Les fichiers d’archive de texte peuvent être utilisés avec les systèmes de gestion de version.</span><span class="sxs-lookup"><span data-stu-id="e07bf-111">Text archive files can be used with version control systems.</span></span>
-   <span data-ttu-id="e07bf-112">Pour supprimer l’espace de stockage gaspillé et réduire la taille finale des fichiers. msi.</span><span class="sxs-lookup"><span data-stu-id="e07bf-112">To remove wasted storage space and reduce the final size of .msi files.</span></span> <span data-ttu-id="e07bf-113">Consultez [réduction de la taille d’un fichier. msi](reducing-the-size-of-an--msi-file.md).</span><span class="sxs-lookup"><span data-stu-id="e07bf-113">See [Reducing the Size of an .msi File](reducing-the-size-of-an--msi-file.md).</span></span>
-   <span data-ttu-id="e07bf-114">Pour ajouter des informations de localisation à une base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="e07bf-114">To add localization information to an installation database.</span></span> <span data-ttu-id="e07bf-115">Pour plus d’informations, consultez [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e07bf-115">For more information, see [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

-   <span data-ttu-id="e07bf-116">Pour déterminer la page de codes d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="e07bf-116">To determine the code page of a database.</span></span> <span data-ttu-id="e07bf-117">Consultez [détermination de la page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="e07bf-117">See [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md).</span></span>
-   <span data-ttu-id="e07bf-118">Pour définir la page de codes d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="e07bf-118">To set the code page of a database.</span></span> <span data-ttu-id="e07bf-119">Consultez [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="e07bf-119">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="e07bf-120">Pour augmenter la limite d’une colonne de base de données.</span><span class="sxs-lookup"><span data-stu-id="e07bf-120">To increase the limit of a database column.</span></span> <span data-ttu-id="e07bf-121">Exportez la table à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), modifiez le fichier. IDT exporté, puis importez la table à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="e07bf-121">Export the table using [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), edit the exported .idt file, and then import the table using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="e07bf-122">Les auteurs ne peuvent pas modifier les types de données de colonne, les valeurs null ou les attributs de localisation des colonnes dans les tables standard.</span><span class="sxs-lookup"><span data-stu-id="e07bf-122">Authors cannot change the column data types, nullability, or localization attributes of any columns in standard tables.</span></span> <span data-ttu-id="e07bf-123">Consultez également [création d’un package volumineux](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="e07bf-123">See also [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="e07bf-124">Les pages suivantes décrivent les pages d’archive de texte et leurs formats.</span><span class="sxs-lookup"><span data-stu-id="e07bf-124">The following pages describe text archive pages and their formats.</span></span>

-   [<span data-ttu-id="e07bf-125">Format de fichier d’archive</span><span class="sxs-lookup"><span data-stu-id="e07bf-125">Archive File Format</span></span>](archive-file-format.md)
-   [<span data-ttu-id="e07bf-126">Données ASCII dans les fichiers d’archive de texte</span><span class="sxs-lookup"><span data-stu-id="e07bf-126">ASCII Data in Text Archive Files</span></span>](ascii-data-in-text-archive-files.md)
-   [<span data-ttu-id="e07bf-127">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="e07bf-127">\_ForceCodepage</span></span>](-forcecodepage.md)
-   [<span data-ttu-id="e07bf-128">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="e07bf-128">\_SummaryInformation</span></span>](-summaryinformation.md)

 

 



