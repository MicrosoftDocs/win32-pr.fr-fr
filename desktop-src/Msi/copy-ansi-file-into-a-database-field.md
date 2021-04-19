---
description: L’exemple de fichier de code VBScript WiTextIn.vbs est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: Copier le fichier ANSI dans un champ de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541832"
---
# <a name="copy-ansi-file-into-a-database-field"></a><span data-ttu-id="2a854-103">Copier le fichier ANSI dans un champ de base de données</span><span class="sxs-lookup"><span data-stu-id="2a854-103">Copy ANSI File Into a Database Field</span></span>

<span data-ttu-id="2a854-104">L’exemple de fichier de code VBScript WiTextIn.vbs est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2a854-104">The VBScript code sample file WiTextIn.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="2a854-105">L’exemple montre comment utiliser un script pour copier un fichier dans un champ de texte d’une base de données Windows Installer, et illustre le traitement des données de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="2a854-105">The sample shows how a script can be used to copy a file into a text field of a Windows Installer database, and demonstrates the processing of primary key data.</span></span>

<span data-ttu-id="2a854-106">L’exemple de code vous montre également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2a854-106">The code sample also shows you the following:</span></span>

-   <span data-ttu-id="2a854-107">[**OpenDatabase, méthode (objet installer)**](installer-opendatabase.md) et [**méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [**objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="2a854-107">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md) and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="2a854-108">[**Méthode OpenView**](database-openview.md), [**méthode Commit**](database-commit.md)et [**propriété PrimaryKeys**](database-primarykeys.md) de l' [**objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="2a854-108">[**OpenView method**](database-openview.md), the [**Commit method**](database-commit.md), and the [**PrimaryKeys property**](database-primarykeys.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="2a854-109">[**Méthode fetch**](view-fetch.md) et [**méthode modify**](view-modify.md) de l' [**objet View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="2a854-109">[**Fetch method**](view-fetch.md) and the [**Modify method**](view-modify.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="2a854-110">[**Propriété StringData**](record-stringdata.md) et [**méthode ReadStream**](record-readstream.md) de l' [**objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="2a854-110">[**StringData property**](record-stringdata.md) and [**ReadStream method**](record-readstream.md) of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="2a854-111">Pour utiliser l’exemple de code, vous avez besoin de la version CScript.exe ou WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="2a854-111">To use the code sample you need the CScript.exe or WScript.exe version of Windows Script Host.</span></span>

<span data-ttu-id="2a854-112">**Pour utiliser CScript.exe pour exécuter cet exemple**</span><span class="sxs-lookup"><span data-stu-id="2a854-112">**To use CScript.exe to run this sample**</span></span>

-   <span data-ttu-id="2a854-113">À l’invite de commandes, tapez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2a854-113">At the command prompt, type the following syntax:</span></span>

    <span data-ttu-id="2a854-114">**cscript WiTextIn.vbs \[ chemin d’accès au nom de la table de base de données \] \[ \] \[ valeurs de clé primaire \] \[ chemin d' \] \[ accès au fichier\]**</span><span class="sxs-lookup"><span data-stu-id="2a854-114">**cscript WiTextIn.vbs \[path to database\]\[table name\]\[primary key values\]\[column name\]\[path to file\]**</span></span>

> [!Note]  
> <span data-ttu-id="2a854-115">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="2a854-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="2a854-116">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="2a854-116">or if too few arguments are specified.</span></span>

 

<span data-ttu-id="2a854-117">**Pour rediriger la sortie vers un fichier**</span><span class="sxs-lookup"><span data-stu-id="2a854-117">**To redirect the output to a file**</span></span>

-   <span data-ttu-id="2a854-118">Terminez la ligne de commande avec les éléments suivants : **VBS > \[ chemin d’accès au fichier \] . T**</span><span class="sxs-lookup"><span data-stu-id="2a854-118">End the command line with the following: **VBS > \[path to file\]. T**</span></span>

> [!Note]  
> <span data-ttu-id="2a854-119">L’exemple retourne la valeur 0 (zéro) pour Success, 1 (un) si l’aide est appelée, et 2 (deux) si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="2a854-119">The sample returns a value of 0 (zero) for success, 1 (one) if Help is invoked, and 2 (two) if the script fails.</span></span>

 

<span data-ttu-id="2a854-120">La liste suivante identifie les éléments que vous devez spécifier :</span><span class="sxs-lookup"><span data-stu-id="2a854-120">The following list identifies the items that you must specify:</span></span>

-   <span data-ttu-id="2a854-121">Spécifiez le chemin d’accès à la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2a854-121">Specify the path to the Windows Installer database.</span></span>
-   <span data-ttu-id="2a854-122">Spécifiez le nom de la table de base de données.</span><span class="sxs-lookup"><span data-stu-id="2a854-122">Specify the name of the database table.</span></span>
-   <span data-ttu-id="2a854-123">Spécifiez toutes les valeurs de clé primaire pour la ligne, dans l’ordre, et concaténées avec les signes deux-points.</span><span class="sxs-lookup"><span data-stu-id="2a854-123">Specify all the primary key values for the row, in order, and concatenated with colons.</span></span>
-   <span data-ttu-id="2a854-124">Spécifiez un nom de colonne qui n’est pas une colonne clé.</span><span class="sxs-lookup"><span data-stu-id="2a854-124">Specify a column name that is not a key column.</span></span> <span data-ttu-id="2a854-125">Il s’agit de la colonne à laquelle vous souhaitez recevoir les données.</span><span class="sxs-lookup"><span data-stu-id="2a854-125">This is the column that you want to receive the data.</span></span>
-   <span data-ttu-id="2a854-126">Spécifiez le chemin d’accès au fichier texte copié.</span><span class="sxs-lookup"><span data-stu-id="2a854-126">Specify the path to the text file that is being copied.</span></span>

> [!Note]  
> <span data-ttu-id="2a854-127">Si le dernier argument est omis, la valeur actuelle dans le champ est affichée.</span><span class="sxs-lookup"><span data-stu-id="2a854-127">If the last argument is omitted, the current value in the field is displayed.</span></span>

 

<span data-ttu-id="2a854-128">Pour obtenir d’autres exemples de script, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="2a854-128">For more scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="2a854-129">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas l’environnement d’exécution de scripts Windows, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2a854-129">For sample utilities that do not require the Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



