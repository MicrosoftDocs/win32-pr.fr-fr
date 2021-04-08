---
description: Les diagrammes de flow des sections suivantes illustrent les règles de contrôle de version de fichier par défaut utilisées lorsque le fichier de clé d’un composant en cours d’installation a le même nom qu’un fichier déjà installé à l’emplacement cible.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Contrôle de version de fichier par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866361"
---
# <a name="default-file-versioning"></a><span data-ttu-id="4e266-103">Contrôle de version de fichier par défaut</span><span class="sxs-lookup"><span data-stu-id="4e266-103">Default File Versioning</span></span>

<span data-ttu-id="4e266-104">Les diagrammes de flow des sections suivantes illustrent les règles de contrôle de version de fichier par défaut utilisées lorsque le fichier de clé d’un composant en cours d’installation a le même nom qu’un fichier déjà installé à l’emplacement cible.</span><span class="sxs-lookup"><span data-stu-id="4e266-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="4e266-105">Le contrôle de version de fichier par défaut est également illustré dans le [remplacement de fichiers existants](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="4e266-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="4e266-106">Notez qu’avec Windows Installer, le hachage de fichier est disponible pour optimiser la copie des fichiers.</span><span class="sxs-lookup"><span data-stu-id="4e266-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="4e266-107">Pour plus d’informations, consultez [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) et la [table MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="4e266-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="4e266-108">La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.</span><span class="sxs-lookup"><span data-stu-id="4e266-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="4e266-109">Les deux fichiers ont une version</span><span class="sxs-lookup"><span data-stu-id="4e266-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="4e266-110">Aucun fichier n’a une version</span><span class="sxs-lookup"><span data-stu-id="4e266-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="4e266-111">Aucun fichier n’a une version avec contrôle de hachage de fichier</span><span class="sxs-lookup"><span data-stu-id="4e266-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="4e266-112">Un fichier a une version</span><span class="sxs-lookup"><span data-stu-id="4e266-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



