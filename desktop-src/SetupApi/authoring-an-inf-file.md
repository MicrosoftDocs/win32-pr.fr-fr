---
description: Lors de la création d’un fichier INF pour une application d’installation, vous devez également vous reporter au format de fichier INF documenté dans instructions générales pour les fichiers INF et les sections et directives du fichier INF du kit de développement de pilotes Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Création d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517253"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="782d6-103">Création d’un fichier INF</span><span class="sxs-lookup"><span data-stu-id="782d6-103">Authoring an INF file</span></span>

<span data-ttu-id="782d6-104">Lors de la création d’un fichier INF pour une application d’installation, vous devez également vous reporter au format de fichier INF documenté dans *instructions générales pour les fichiers INF* et les *sections et directives du fichier* INF du kit de développement de pilotes Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="782d6-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="782d6-105">Lors de la création de fichiers INF pour une application d’installation, respectez les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="782d6-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="782d6-106">Une section **version** est requise dans chaque fichier INF.</span><span class="sxs-lookup"><span data-stu-id="782d6-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="782d6-107">Les sections doivent commencer par le nom de la section entre crochets ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="782d6-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="782d6-108">Les noms des sections **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** et **version** doivent être identiques au type de section.</span><span class="sxs-lookup"><span data-stu-id="782d6-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="782d6-109">Par exemple \[ , utilisez DestinationDirs \] .</span><span class="sxs-lookup"><span data-stu-id="782d6-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="782d6-110">Les auteurs peuvent spécifier les noms d’autres types de sections.</span><span class="sxs-lookup"><span data-stu-id="782d6-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="782d6-111">Les noms des sections **SourceDisksNames** et **SourceDisksFiles** peuvent être ajoutés avec un suffixe spécifique à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="782d6-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="782d6-112">Par exemple, pour afficher une section **SourceDisksNames** spécifique à Intel, utilisez \[ SourceDisksNames. x86 \] .</span><span class="sxs-lookup"><span data-stu-id="782d6-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="782d6-113">Si les fonctions d’installation recherchent des sections **SourceDisksNames** et **SourceDisksFiles** spécifiques à la plateforme correspondant à la plate-forme de l’utilisateur, les fonctions utilisent les sections spécifiques à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="782d6-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="782d6-114">Dans le cas contraire, les fonctions d’installation utilisent les sections **SourceDisksNames** et **SourceDisksFiles** sans suffixe.</span><span class="sxs-lookup"><span data-stu-id="782d6-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="782d6-115">Les fonctions d’installation peuvent déterminer par programme le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="782d6-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="782d6-116">Consultez l' [exemple de sections INF SourceDisksNames et SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span><span class="sxs-lookup"><span data-stu-id="782d6-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="782d6-117">Les valeurs peuvent être exprimées sous forme de chaînes remplaçables au format%*strKey*%.</span><span class="sxs-lookup"><span data-stu-id="782d6-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="782d6-118">Pour utiliser un caractère% dans la chaîne, utilisez%%.</span><span class="sxs-lookup"><span data-stu-id="782d6-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="782d6-119">StrKey doit être défini dans une section **Strings** du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="782d6-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



