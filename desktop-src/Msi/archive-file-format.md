---
description: Un fichier d’archive de texte pour une base de données Windows Installer comporte une extension de nom de fichier. IDT.
ms.assetid: 91d81fb2-3a41-477a-85c2-e68bfe482b9c
title: Format de fichier d’archive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf39383b961c305bf621793784332342f369a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864470"
---
# <a name="archive-file-format"></a><span data-ttu-id="d6d43-103">Format de fichier d’archive</span><span class="sxs-lookup"><span data-stu-id="d6d43-103">Archive File Format</span></span>

<span data-ttu-id="d6d43-104">Un [fichier d’archive de texte](text-archive-files.md) pour une base de données Windows Installer comporte une extension de nom de fichier. IDT.</span><span class="sxs-lookup"><span data-stu-id="d6d43-104">A [text archive file](text-archive-files.md) for a Windows Installer database carries an .idt file name extension.</span></span> <span data-ttu-id="d6d43-105">Lorsqu’une base de données entière est exportée vers des fichiers d’archive, chaque table de la base de données a un fichier. IDT distinct.</span><span class="sxs-lookup"><span data-stu-id="d6d43-105">When an entire database is exported to archive files, each table in the database has a separate .idt file.</span></span> <span data-ttu-id="d6d43-106">Si une table contient une colonne de flux, chaque flux de la table est représenté par un fichier avec une extension de nom de fichier. IBD.</span><span class="sxs-lookup"><span data-stu-id="d6d43-106">If a table contains a stream column, each stream in the table is represented by a file with an .ibd file name extension.</span></span> <span data-ttu-id="d6d43-107">Les fichiers. IBD sont stockés dans un dossier portant le même nom que la table.</span><span class="sxs-lookup"><span data-stu-id="d6d43-107">The .ibd files are stored in a folder with the same name as the table.</span></span>

## <a name="idt-file-format"></a><span data-ttu-id="d6d43-108">Format de fichier. IDT</span><span class="sxs-lookup"><span data-stu-id="d6d43-108">.idt File Format</span></span>

<span data-ttu-id="d6d43-109">Le fichier. IDT d’une table de base de données exportée qui contient uniquement des caractères ASCII a le format de base suivant.</span><span class="sxs-lookup"><span data-stu-id="d6d43-109">The .idt file of an exported database table that contains only ASCII characters has the following basic format.</span></span>

-   <span data-ttu-id="d6d43-110">La première ligne contient les noms de colonnes de table séparés par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="d6d43-110">The first row contains the table column names separated by tabs.</span></span>
-   <span data-ttu-id="d6d43-111">La deuxième ligne contient les définitions de colonne séparées par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="d6d43-111">The second row contains the column definitions separated by tabs.</span></span>
-   <span data-ttu-id="d6d43-112">Si le fichier contient uniquement des données ASCII, la troisième ligne est le nom de la table et les noms de colonne de clé primaire séparés par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="d6d43-112">If the file contain only ASCII data, the third row is table name and primary key column names separated by tabs.</span></span>
-   <span data-ttu-id="d6d43-113">Les lignes restantes dans le fichier représentent des lignes de la table, avec des colonnes séparées par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="d6d43-113">The remaining rows in the file represent rows in the table, with columns separated by tabs.</span></span>

> [!Note]  
> <span data-ttu-id="d6d43-114">Si le fichier contient des données non-ASCII, la troisième ligne correspond à la page de codes numérique suivie du nom de la table et des noms de colonne de clé primaire séparés par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="d6d43-114">If the file contains non-ASCII data, the third row is the numeric code page followed by the table name and primary key column names separated by tabs.</span></span> <span data-ttu-id="d6d43-115">Un fichier. IDT qui contient des informations non-ASCII doit être enregistré au format ASCII.</span><span class="sxs-lookup"><span data-stu-id="d6d43-115">An .idt file that contains non-ASCII information should be saved in the ASCII format.</span></span> <span data-ttu-id="d6d43-116">Par exemple, un fichier d’archive de texte peut contenir les noms de colonne et de table encodés au format UTF-8, mais le fichier d’archive lui-même doit être au format ASCII.</span><span class="sxs-lookup"><span data-stu-id="d6d43-116">For example, a text archive file can contain the column and table names encoded as UTF-8, but the archive file itself should be ASCII.</span></span> <span data-ttu-id="d6d43-117">Consultez la section [données ASCII dans les fichiers d’archive de texte](ascii-data-in-text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="d6d43-117">See the section [ASCII Data in Text Archive Files](ascii-data-in-text-archive-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="d6d43-118">Les fichiers [ \_ ForceCodepage](-forcecodepage.md) et [ \_ SummaryInformation](-summaryinformation.md) . IDT spéciaux utilisent des formats étendus.</span><span class="sxs-lookup"><span data-stu-id="d6d43-118">The special [\_ForceCodepage](-forcecodepage.md) and [\_SummaryInformation](-summaryinformation.md) .idt files use extended formats.</span></span> <span data-ttu-id="d6d43-119">Consultez les \_ sections ForceCodepage et \_ SummaryInformation pour obtenir une description de leurs formats.</span><span class="sxs-lookup"><span data-stu-id="d6d43-119">See the \_ForceCodepage and \_SummaryInformation sections for descriptions of their formats.</span></span>

 

## <a name="column-definitions"></a><span data-ttu-id="d6d43-120">Définitions de colonne</span><span class="sxs-lookup"><span data-stu-id="d6d43-120">Column Definitions</span></span>

<span data-ttu-id="d6d43-121">Les définitions de colonne sont indiquées par des caractères.</span><span class="sxs-lookup"><span data-stu-id="d6d43-121">Column definitions are indicated by characters.</span></span>

-   <span data-ttu-id="d6d43-122">Le premier caractère indique le type de colonne.</span><span class="sxs-lookup"><span data-stu-id="d6d43-122">The first character indicates the column type.</span></span> <span data-ttu-id="d6d43-123">Une lettre minuscule indique une colonne qui n’accepte pas les valeurs NULL et une lettre majuscule indique que la colonne peut contenir des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="d6d43-123">A lowercase letter indicates a non-nullable column and an uppercase letter indicates that the column can contain null values.</span></span>

    | <span data-ttu-id="d6d43-124">Caractère</span><span class="sxs-lookup"><span data-stu-id="d6d43-124">Character</span></span> | <span data-ttu-id="d6d43-125">Signification</span><span class="sxs-lookup"><span data-stu-id="d6d43-125">Meaning</span></span>                   |
    |-----------|---------------------------|
    | <span data-ttu-id="d6d43-126">s, S</span><span class="sxs-lookup"><span data-stu-id="d6d43-126">s, S</span></span>      | <span data-ttu-id="d6d43-127">Colonne de chaîne</span><span class="sxs-lookup"><span data-stu-id="d6d43-127">String Column</span></span>             |
    | <span data-ttu-id="d6d43-128">l, L</span><span class="sxs-lookup"><span data-stu-id="d6d43-128">l, L</span></span>      | <span data-ttu-id="d6d43-129">Colonne de chaîne localisable</span><span class="sxs-lookup"><span data-stu-id="d6d43-129">Localizable String Column</span></span> |
    | <span data-ttu-id="d6d43-130">v, V</span><span class="sxs-lookup"><span data-stu-id="d6d43-130">v, V</span></span>      | <span data-ttu-id="d6d43-131">Colonne binaire</span><span class="sxs-lookup"><span data-stu-id="d6d43-131">Binary Column</span></span>             |
    | <span data-ttu-id="d6d43-132">Je vais</span><span class="sxs-lookup"><span data-stu-id="d6d43-132">i, I</span></span>      | <span data-ttu-id="d6d43-133">Colonne d’entiers</span><span class="sxs-lookup"><span data-stu-id="d6d43-133">Integer Column</span></span>            |

    

     

-   <span data-ttu-id="d6d43-134">Le deuxième caractère indique la taille des données de la colonne.</span><span class="sxs-lookup"><span data-stu-id="d6d43-134">The second character indicates the column data size.</span></span>

    > [!Note]  
    > <span data-ttu-id="d6d43-135">La Windows Installer n’utilise pas réellement la taille de colonne spécifiée pour limiter la taille de la chaîne qui peut être entrée dans un champ de colonne de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d6d43-135">The Windows Installer does not actually use the specified column size to limit the size of the string that can be entered into a string column field.</span></span> <span data-ttu-id="d6d43-136">Toutefois, certains outils de création utilisent la taille de colonne spécifiée pour limiter la taille d’une chaîne valide.</span><span class="sxs-lookup"><span data-stu-id="d6d43-136">However, some authoring tools do use the specified column size to limit the size of a valid string.</span></span> <span data-ttu-id="d6d43-137">Il est recommandé que les chaînes entrées dans une colonne répondent à l’exigence de taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d6d43-137">It is recommended that strings entered into any column meet the specified size requirement.</span></span>

     

    

    | <span data-ttu-id="d6d43-138">Définition de colonne</span><span class="sxs-lookup"><span data-stu-id="d6d43-138">Column Definition</span></span> | <span data-ttu-id="d6d43-139">Signification</span><span class="sxs-lookup"><span data-stu-id="d6d43-139">Meaning</span></span>                                    |
    |-------------------|--------------------------------------------|
    | <span data-ttu-id="d6d43-140">s255</span><span class="sxs-lookup"><span data-stu-id="d6d43-140">s255</span></span>              | <span data-ttu-id="d6d43-141">Colonne de chaîne non Nullable 255 longue</span><span class="sxs-lookup"><span data-stu-id="d6d43-141">Non-Nullable String Column 255 long</span></span>        |
    | <span data-ttu-id="d6d43-142">L50</span><span class="sxs-lookup"><span data-stu-id="d6d43-142">L50</span></span>               | <span data-ttu-id="d6d43-143">Colonne de chaîne localisable Nullable 50 long</span><span class="sxs-lookup"><span data-stu-id="d6d43-143">Nullable Localizable String Column 50 long</span></span> |
    | <span data-ttu-id="d6d43-144">I2, I2</span><span class="sxs-lookup"><span data-stu-id="d6d43-144">i2, I2</span></span>            | <span data-ttu-id="d6d43-145">Colonne de type entier Short</span><span class="sxs-lookup"><span data-stu-id="d6d43-145">Short Integer Column</span></span>                       |
    | <span data-ttu-id="d6d43-146">I4, I4</span><span class="sxs-lookup"><span data-stu-id="d6d43-146">i4, I4</span></span>            | <span data-ttu-id="d6d43-147">Colonne de type entier long</span><span class="sxs-lookup"><span data-stu-id="d6d43-147">Long Integer Column</span></span>                        |

    

     

## <a name="control-character-translation"></a><span data-ttu-id="d6d43-148">Conversion de caractères de contrôle</span><span class="sxs-lookup"><span data-stu-id="d6d43-148">Control Character Translation</span></span>

<span data-ttu-id="d6d43-149">L’exportation d’une table dans un fichier d’archive de texte traduit les caractères de contrôle pour éviter les conflits avec les délimiteurs de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d6d43-149">Exporting a table to a text archive file translates the control characters to avoid conflicts with file delimiters.</span></span> <span data-ttu-id="d6d43-150">Lors de l’écriture dans le fichier. IDT, les caractères de contrôle sont convertis comme suit.</span><span class="sxs-lookup"><span data-stu-id="d6d43-150">While writing into the .idt file, the control characters are translated as follows.</span></span>



| <span data-ttu-id="d6d43-151">Caractère de contrôle</span><span class="sxs-lookup"><span data-stu-id="d6d43-151">Control Character</span></span> | <span data-ttu-id="d6d43-152">Traduction dans. IDT</span><span class="sxs-lookup"><span data-stu-id="d6d43-152">Translation in .idt</span></span> | <span data-ttu-id="d6d43-153">Signification</span><span class="sxs-lookup"><span data-stu-id="d6d43-153">Meaning</span></span>         |
|-------------------|---------------------|-----------------|
| <span data-ttu-id="d6d43-154">NULL</span><span class="sxs-lookup"><span data-stu-id="d6d43-154">NULL</span></span>              | <span data-ttu-id="d6d43-155">21</span><span class="sxs-lookup"><span data-stu-id="d6d43-155">21</span></span>                  | <span data-ttu-id="d6d43-156">Null</span><span class="sxs-lookup"><span data-stu-id="d6d43-156">Null</span></span>            |
| <span data-ttu-id="d6d43-157">BS</span><span class="sxs-lookup"><span data-stu-id="d6d43-157">BS</span></span>                | <span data-ttu-id="d6d43-158">27</span><span class="sxs-lookup"><span data-stu-id="d6d43-158">27</span></span>                  | <span data-ttu-id="d6d43-159">Espace arrière</span><span class="sxs-lookup"><span data-stu-id="d6d43-159">Back Space</span></span>      |
| <span data-ttu-id="d6d43-160">HT</span><span class="sxs-lookup"><span data-stu-id="d6d43-160">HT</span></span>                | <span data-ttu-id="d6d43-161">16</span><span class="sxs-lookup"><span data-stu-id="d6d43-161">16</span></span>                  | <span data-ttu-id="d6d43-162">Onglet</span><span class="sxs-lookup"><span data-stu-id="d6d43-162">Tab</span></span>             |
| <span data-ttu-id="d6d43-163">CHARIOT</span><span class="sxs-lookup"><span data-stu-id="d6d43-163">LF</span></span>                | <span data-ttu-id="d6d43-164">25</span><span class="sxs-lookup"><span data-stu-id="d6d43-164">25</span></span>                  | <span data-ttu-id="d6d43-165">Saut de ligne</span><span class="sxs-lookup"><span data-stu-id="d6d43-165">Line Feed</span></span>       |
| <span data-ttu-id="d6d43-166">FF</span><span class="sxs-lookup"><span data-stu-id="d6d43-166">FF</span></span>                | <span data-ttu-id="d6d43-167">24</span><span class="sxs-lookup"><span data-stu-id="d6d43-167">24</span></span>                  | <span data-ttu-id="d6d43-168">Flux de formulaire</span><span class="sxs-lookup"><span data-stu-id="d6d43-168">Form Feed</span></span>       |
| <span data-ttu-id="d6d43-169">CR</span><span class="sxs-lookup"><span data-stu-id="d6d43-169">CR</span></span>                | <span data-ttu-id="d6d43-170">17</span><span class="sxs-lookup"><span data-stu-id="d6d43-170">17</span></span>                  | <span data-ttu-id="d6d43-171">Retour chariot</span><span class="sxs-lookup"><span data-stu-id="d6d43-171">Carriage Return</span></span> |



 

 

 



