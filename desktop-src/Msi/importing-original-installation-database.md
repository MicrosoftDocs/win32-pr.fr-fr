---
description: Commencez à créer le package de mise à niveau en copiant le package d’installation et l’arborescence du répertoire source du produit d’origine.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importation de la base de données d’installation d’origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521836"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="4a11c-103">Importation de la base de données d’installation d’origine</span><span class="sxs-lookup"><span data-stu-id="4a11c-103">Importing Original Installation Database</span></span>

<span data-ttu-id="4a11c-104">Commencez à créer le package de mise à niveau en copiant le package d’installation et l’arborescence du répertoire source du produit d’origine.</span><span class="sxs-lookup"><span data-stu-id="4a11c-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="4a11c-105">Des instructions sur la création du package d’installation pour MNP2000 sont fournies dans [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="4a11c-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="4a11c-106">Vous devez copier le contenu des dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="4a11c-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="4a11c-107">C : \\ exemple de \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="4a11c-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="4a11c-108">C : \\ exemple de \\ bloc-notes</span><span class="sxs-lookup"><span data-stu-id="4a11c-108">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="4a11c-109">C : \\ exemple de \\ binaire</span><span class="sxs-lookup"><span data-stu-id="4a11c-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="4a11c-110">C : \\ exemple d' \\ icône</span><span class="sxs-lookup"><span data-stu-id="4a11c-110">C:\\Sample\\Icon</span></span>\\

<span data-ttu-id="4a11c-111">Mettez à jour le contenu du dossier Notepad afin qu’il corresponde à la source décrite dans [planification d’une mise à niveau majeure](planning-a-major-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="4a11c-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="4a11c-112">Supprimez tous les fichiers sources obsolètes, tels que Baseball.txt, et remplacez par les fichiers mis à jour, tels que Baseba01.txt.</span><span class="sxs-lookup"><span data-stu-id="4a11c-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="4a11c-113">Ajoutez les nouveaux fichiers supplémentaires fournis par la mise à niveau, par exemple Opera01.txt.</span><span class="sxs-lookup"><span data-stu-id="4a11c-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="4a11c-114">Renommez MNP2000.msi MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="4a11c-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="4a11c-115">Dans les étapes suivantes, vous allez utiliser un éditeur de table pour modifier cette base de données dans le fichier. msi pour la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="4a11c-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="4a11c-116">Les tables de base de données qui ne sont pas explicitement modifiées dans les sections suivantes sont identiques aux tables de la base de données du produit d’origine, MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="4a11c-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="4a11c-117">Continuer</span><span class="sxs-lookup"><span data-stu-id="4a11c-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



