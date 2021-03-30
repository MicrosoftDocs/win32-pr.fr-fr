---
description: Windows 7 présente des bibliothèques, qui fournissent aux utilisateurs une vue unique et cohérente de leurs fichiers, même lorsque ces fichiers sont stockés dans des emplacements différents.
title: Bibliothèques Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973839"
---
# <a name="windows-libraries"></a><span data-ttu-id="71531-103">Bibliothèques Windows</span><span class="sxs-lookup"><span data-stu-id="71531-103">Windows Libraries</span></span>

<span data-ttu-id="71531-104">Windows 7 présente des bibliothèques, qui fournissent aux utilisateurs une vue unique et cohérente de leurs fichiers, même lorsque ces fichiers sont stockés dans des emplacements différents.</span><span class="sxs-lookup"><span data-stu-id="71531-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="71531-105">Les bibliothèques peuvent être configurées et organisées par un utilisateur et une bibliothèque peut contenir des dossiers qui se trouvent sur l’ordinateur de l’utilisateur et également des dossiers qui ont été partagés sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="71531-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="71531-106">Les bibliothèques présentent une vue plus simple du système de stockage sous-jacent car, pour l’utilisateur, les fichiers et les dossiers d’une bibliothèque s’affichent dans une seule vue, quel que soit l’emplacement où ils sont stockés physiquement.</span><span class="sxs-lookup"><span data-stu-id="71531-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="71531-107">Les développeurs qui écrivent de nouveaux programmes dans Windows 7 sont encouragés à utiliser des bibliothèques comme moyen permettant aux utilisateurs d’interagir avec les fichiers utilisés par le programme.</span><span class="sxs-lookup"><span data-stu-id="71531-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="71531-108">L’utilisation de bibliothèques dans votre programme offre aux utilisateurs une expérience plus propre, plus simple et plus cohérente dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71531-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="71531-109">Les développeurs doivent également examiner leurs programmes existants et les mettre à jour si nécessaire, pour travailler avec des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="71531-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="71531-110">Étant donné que les bibliothèques ne font pas partie du système de fichiers, les API basées sur le système de fichiers n’ont pas accès aux bibliothèques que l’utilisateur a pu configurer.</span><span class="sxs-lookup"><span data-stu-id="71531-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="71531-111">Les programmes qui permettent actuellement aux utilisateurs de stocker leur contenu dans différents dossiers ou sur des ordinateurs différents tireront le meilleur parti lorsqu’ils ajoutent la prise en charge de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="71531-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="71531-112">Les bibliothèques simplifient la gestion du contenu dans divers emplacements de stockage pour le développeur et l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71531-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="71531-113">Ce guide décrit en détail les bibliothèques, la façon dont les programmes peuvent être utilisés pour travailler avec les bibliothèques, ainsi que certains des moyens dont dispose un programme pour améliorer l’expérience de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71531-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71531-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71531-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71531-115">À propos des bibliothèques</span><span class="sxs-lookup"><span data-stu-id="71531-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="71531-116">Utilisation de bibliothèques dans votre programme</span><span class="sxs-lookup"><span data-stu-id="71531-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="71531-117">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="71531-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="71531-118">Liens de Shell</span><span class="sxs-lookup"><span data-stu-id="71531-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="71531-119">Dossiers connus</span><span class="sxs-lookup"><span data-stu-id="71531-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="71531-120">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71531-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
