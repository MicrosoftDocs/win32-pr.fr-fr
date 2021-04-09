---
description: L’état d’installation d’un fichier associé ne dépend pas de ses propres informations de contrôle de version de fichier, mais du contrôle de version de son parent associé.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Fichiers auxiliaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952517"
---
# <a name="companion-files"></a><span data-ttu-id="a6f73-103">Fichiers auxiliaires</span><span class="sxs-lookup"><span data-stu-id="a6f73-103">Companion Files</span></span>

<span data-ttu-id="a6f73-104">L’état d’installation d’un fichier associé ne dépend pas de ses propres informations de contrôle de version de fichier, mais du contrôle de version de son parent associé.</span><span class="sxs-lookup"><span data-stu-id="a6f73-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="a6f73-105">Consultez les [règles](file-versioning-rules.md)de contrôle de version des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a6f73-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="a6f73-106">Pour spécifier un fichier compagnon, la clé primaire du parent compagnon dans la [table file](file-table.md) doit être créée dans la colonne version de l’enregistrement pour le compagnon.</span><span class="sxs-lookup"><span data-stu-id="a6f73-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="a6f73-107">Dans l’exemple suivant, Filea est le parent associé et FileB est le fichier associé.</span><span class="sxs-lookup"><span data-stu-id="a6f73-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="a6f73-108">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="a6f73-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="a6f73-109">Fichier</span><span class="sxs-lookup"><span data-stu-id="a6f73-109">File</span></span>  | <span data-ttu-id="a6f73-110">Version</span><span class="sxs-lookup"><span data-stu-id="a6f73-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="a6f73-111">Filea</span><span class="sxs-lookup"><span data-stu-id="a6f73-111">FileA</span></span> | <span data-ttu-id="a6f73-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="a6f73-112">1.0.0.0</span></span> |
| <span data-ttu-id="a6f73-113">FileB</span><span class="sxs-lookup"><span data-stu-id="a6f73-113">FileB</span></span> | <span data-ttu-id="a6f73-114">Filea</span><span class="sxs-lookup"><span data-stu-id="a6f73-114">FileA</span></span>   |



 

<span data-ttu-id="a6f73-115">Dans cet exemple, l’état d’installation de FileB dépend des [règles](file-versioning-rules.md) de contrôle de version des fichiers et des informations de contrôle de version pour Filea.</span><span class="sxs-lookup"><span data-stu-id="a6f73-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="a6f73-116">Si le programme d’installation détermine que la version de Filea dans le package doit être installée sur une version antérieure de Filea qui existe déjà sur l’ordinateur de l’utilisateur, il installera également FileB à partir du package, quelle que soit la version des FileB installés.</span><span class="sxs-lookup"><span data-stu-id="a6f73-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="a6f73-117">Notez qu’un fichier qui est le chemin d’accès de clé de son composant ne doit pas être un fichier auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="a6f73-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="a6f73-118">Cela entraînerait la logique de contrôle de version du fichier de chemin d’accès de clé qui est déterminée par le fichier parent associé.</span><span class="sxs-lookup"><span data-stu-id="a6f73-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



