---
description: Chaque fichier qui est remis au package d’installation cible par le module de fusion doit être stocké dans un fichier CAB incorporé en tant que flux à l’intérieur du fichier. msm. Le nom de ce fichier cab est toujours MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Génération de fichiers CAB inet MergeModule.CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521035"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="6f621-104">Génération de fichiers CAB inet MergeModule.CAB</span><span class="sxs-lookup"><span data-stu-id="6f621-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="6f621-105">Chaque fichier qui est remis au package d’installation cible par le module de fusion doit être stocké dans un fichier CAB incorporé en tant que flux à l’intérieur du fichier. msm.</span><span class="sxs-lookup"><span data-stu-id="6f621-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="6f621-106">Le nom de ce fichier cab est toujours MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="6f621-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="6f621-107">Les noms des fichiers dans MergeModule.CABinet doivent correspondre aux clés primaires utilisées dans la [table de fichiers](file-table.md) du module de fusion et doivent respecter la convention décrite dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="6f621-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="6f621-108">Le programme d’installation ignore les fichiers supplémentaires inclus dans MergeModule.CABinet qui ne sont pas répertoriés dans la [table de fichiers](file-table.md)du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="6f621-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="6f621-109">Les numéros de séquence des fichiers spécifiés dans la table de fichiers n’ont pas besoin d’être consécutifs, mais ils doivent suivre la même séquence que les fichiers stockés dans MergeModule.CABinet.</span><span class="sxs-lookup"><span data-stu-id="6f621-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="6f621-110">Pour plus d’informations, consultez [création de tables de fichiers de module de fusion](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6f621-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="6f621-111">Cela signifie qu’un seul fichier CAB peut contenir tous les fichiers nécessaires à un module de fusion pour prendre en charge plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="6f621-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="6f621-112">Tous les fichiers de langue peuvent recevoir des numéros séquentiels uniques dans le fichier CAB, puis une transformation de langue peut être utilisée pour ajouter ou supprimer des fichiers dans la table file afin d’obtenir un module de fusion pour une langue particulière.</span><span class="sxs-lookup"><span data-stu-id="6f621-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="6f621-113">Pour plus d’informations, consultez [création de modules de fusion multilingues](authoring-multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="6f621-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="6f621-114">MergeModule.CABinet peut être ajouté au module de fusion en ouvrant une [ \_ table de flux](-streams-table.md)temporaire.</span><span class="sxs-lookup"><span data-stu-id="6f621-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="6f621-115">Par exemple, l’outil Msidb.exe fourni avec le kit de développement logiciel (SDK) Windows Installer peut être utilisé pour ajouter le MergeModule.CABinet au module de fusion.</span><span class="sxs-lookup"><span data-stu-id="6f621-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="6f621-116">Pour plus d’informations, consultez [inclusion d’un fichier cab dans une installation](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="6f621-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



