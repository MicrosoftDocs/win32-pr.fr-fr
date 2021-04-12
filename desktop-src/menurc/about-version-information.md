---
title: À propos des informations de version
description: Cette rubrique décrit les fonctions d’informations de version.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- ressources, informations sur la version
- informations de version
- ajouter des informations sur la version
- conflits de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381851"
---
# <a name="about-version-information"></a><span data-ttu-id="27fb0-107">À propos des informations de version</span><span class="sxs-lookup"><span data-stu-id="27fb0-107">About Version Information</span></span>

<span data-ttu-id="27fb0-108">Vous pouvez utiliser les fonctions d’informations de version pour déterminer l’emplacement d’installation d’un fichier et identifier les conflits avec les fichiers actuellement installés.</span><span class="sxs-lookup"><span data-stu-id="27fb0-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="27fb0-109">Ces fonctions vous permettent d’éviter les problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="27fb0-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="27fb0-110">installation de versions antérieures de composants sur des versions plus récentes</span><span class="sxs-lookup"><span data-stu-id="27fb0-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="27fb0-111">modification de la langue dans un système mixte sans notification</span><span class="sxs-lookup"><span data-stu-id="27fb0-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="27fb0-112">installation de plusieurs copies d’une bibliothèque dans des répertoires différents</span><span class="sxs-lookup"><span data-stu-id="27fb0-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="27fb0-113">copie de fichiers dans des répertoires réseau partagés par plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="27fb0-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="27fb0-114">Les fonctions d’informations de version permettent aux applications d’interroger une ressource de version pour obtenir des informations sur les fichiers et de présenter les informations dans un format clair.</span><span class="sxs-lookup"><span data-stu-id="27fb0-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="27fb0-115">Ces informations incluent l’objectif du fichier, son auteur, son numéro de version, etc.</span><span class="sxs-lookup"><span data-stu-id="27fb0-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="27fb0-116">Vous pouvez ajouter des informations de version à tous les fichiers qui peuvent avoir des ressources Windows, telles que des dll, des fichiers exécutables ou des fichiers de police. fon.</span><span class="sxs-lookup"><span data-stu-id="27fb0-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="27fb0-117">Pour ajouter les informations, créez une [ressource VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) et utilisez le compilateur de ressources pour compiler la ressource.</span><span class="sxs-lookup"><span data-stu-id="27fb0-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 