---
description: ICE64 vérifie que les nouveaux répertoires du profil utilisateur sont correctement supprimés dans les scénarios d’itinérance.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529584"
---
# <a name="ice64"></a><span data-ttu-id="f44fa-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="f44fa-103">ICE64</span></span>

<span data-ttu-id="f44fa-104">ICE64 vérifie que les nouveaux répertoires du profil utilisateur sont correctement supprimés dans les scénarios d’itinérance.</span><span class="sxs-lookup"><span data-stu-id="f44fa-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="f44fa-105">Si vous ne corrigez pas un avertissement ou une erreur signalée par ICE64, les problèmes surviennent généralement lors de la désinstallation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f44fa-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="f44fa-106">Lorsqu’un utilisateur itinérant qui a installé l’application se connecte à un ordinateur pour la première fois, tout le profil est copié sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f44fa-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="f44fa-107">Sur la publication (qui a lieu après le téléchargement du profil itinérant), le programme d’installation vérifie que le répertoire existe déjà et, par conséquent, ne le supprime pas lors de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f44fa-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="f44fa-108">Cela laisse le répertoire sur l’ordinateur de l’utilisateur de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="f44fa-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="f44fa-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="f44fa-109">Result</span></span>

<span data-ttu-id="f44fa-110">ICE64 publie un avertissement ou une erreur dans une situation d’itinérance si un nouveau répertoire du profil utilisateur à supprimer n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="f44fa-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="f44fa-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="f44fa-111">Example</span></span>

<span data-ttu-id="f44fa-112">ICE64 signale l’erreur suivante pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="f44fa-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="f44fa-113">Le dossier « MyOtherFolder » est un dossier de profil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f44fa-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="f44fa-114">Comme il n’est pas listé dans la table RemoveFile, il n’est pas supprimé dans certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="f44fa-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="f44fa-115">Pour corriger cette erreur, créez une ligne pour le dossier dans la table RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="f44fa-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="f44fa-116">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="f44fa-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="f44fa-117">Répertoire</span><span class="sxs-lookup"><span data-stu-id="f44fa-117">Directory</span></span>     | <span data-ttu-id="f44fa-118">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="f44fa-118">Directory\_Parent</span></span> | <span data-ttu-id="f44fa-119">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="f44fa-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="f44fa-120">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="f44fa-120">AppDataFolder</span></span> | <span data-ttu-id="f44fa-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="f44fa-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="f44fa-122">Mondossier</span><span class="sxs-lookup"><span data-stu-id="f44fa-122">MyFolder</span></span>      | <span data-ttu-id="f44fa-123">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="f44fa-123">AppDataFolder</span></span>     | <span data-ttu-id="f44fa-124">DataFolder</span><span class="sxs-lookup"><span data-stu-id="f44fa-124">DataFolder</span></span>  |
| <span data-ttu-id="f44fa-125">MyOtherFolder</span><span class="sxs-lookup"><span data-stu-id="f44fa-125">MyOtherFolder</span></span> | <span data-ttu-id="f44fa-126">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="f44fa-126">AppDataFolder</span></span>     | <span data-ttu-id="f44fa-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="f44fa-127">DataFolder2</span></span> |



 

[<span data-ttu-id="f44fa-128">Table RemoveFile</span><span class="sxs-lookup"><span data-stu-id="f44fa-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="f44fa-129">FileKey</span><span class="sxs-lookup"><span data-stu-id="f44fa-129">FileKey</span></span> | <span data-ttu-id="f44fa-130">-\_</span><span class="sxs-lookup"><span data-stu-id="f44fa-130">Component\_</span></span> | <span data-ttu-id="f44fa-131">FileName</span><span class="sxs-lookup"><span data-stu-id="f44fa-131">FileName</span></span> | <span data-ttu-id="f44fa-132">DirProperty</span><span class="sxs-lookup"><span data-stu-id="f44fa-132">DirProperty</span></span> | <span data-ttu-id="f44fa-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="f44fa-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="f44fa-134">Clé1</span><span class="sxs-lookup"><span data-stu-id="f44fa-134">Key1</span></span>    | <span data-ttu-id="f44fa-135">Composant1</span><span class="sxs-lookup"><span data-stu-id="f44fa-135">Component1</span></span>  |          | <span data-ttu-id="f44fa-136">Mondossier</span><span class="sxs-lookup"><span data-stu-id="f44fa-136">MyFolder</span></span>    | <span data-ttu-id="f44fa-137">2</span><span class="sxs-lookup"><span data-stu-id="f44fa-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="f44fa-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f44fa-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f44fa-139">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="f44fa-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



