---
description: Utilisez cette instruction pour créer un Windows Installer package contenant plus de 32767 fichiers.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Création d’un package volumineux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518440"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="8a9cd-103">Création d’un package volumineux</span><span class="sxs-lookup"><span data-stu-id="8a9cd-103">Authoring a Large Package</span></span>

<span data-ttu-id="8a9cd-104">Utilisez cette instruction pour créer un Windows Installer package contenant plus de 32767 fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="8a9cd-105">Si votre package Windows Installer contient plus de 32767 fichiers, vous devez modifier le schéma de la base de données pour augmenter la limite des colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a9cd-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="8a9cd-106">Colonne de séquence de la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a9cd-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="8a9cd-107">Colonne LastSequence de la [table multimédia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a9cd-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="8a9cd-108">Colonne de séquence de la [table des correctifs](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="8a9cd-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="8a9cd-109">Pour plus d’informations, consultez [format de définition de colonne](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="8a9cd-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="8a9cd-110">**Pour augmenter la limite d’une colonne de base de données**</span><span class="sxs-lookup"><span data-stu-id="8a9cd-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="8a9cd-111">Exportez la table vers un fichier. IDT.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-111">Export the table to an .idt file.</span></span> <span data-ttu-id="8a9cd-112">Pour plus d’informations, consultez [Msidb.exe](msidb-exe.md), [exporter des fichiers](export-files.md)et [importation et exportation](importing-and-exporting.md).</span><span class="sxs-lookup"><span data-stu-id="8a9cd-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="8a9cd-113">Modifiez le fichier. IDT pour remplacer le type de colonne I2 par i4, ou de I2 par I4.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="8a9cd-114">Exportez la table de [ \_ validation](-validation-table.md) dans un fichier. IDT.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="8a9cd-115">Modifiez le fichier. IDT pour modifier les valeurs de la colonne MaxValue du tableau de [ \_ validation](-validation-table.md) afin de prendre en compte les largeurs de colonne accrues.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="8a9cd-116">Importez de nouveau les fichiers. IDT dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="8a9cd-117">Notez que les transformations et les correctifs ne peuvent pas être créés entre deux packages avec des types de colonnes différents.</span><span class="sxs-lookup"><span data-stu-id="8a9cd-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



