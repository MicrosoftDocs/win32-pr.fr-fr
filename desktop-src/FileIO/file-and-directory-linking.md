---
description: 'Il existe deux types de liens pris en charge dans le système de fichiers NTFS : les liens physiques et les jonctions.'
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: Liaison de fichiers et de répertoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952900"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="c1fe0-103">Liaison de fichiers et de répertoires</span><span class="sxs-lookup"><span data-stu-id="c1fe0-103">File and Directory Linking</span></span>

<span data-ttu-id="c1fe0-104">Le système de fichiers NTFS permet de créer une représentation système d’un fichier ou d’un répertoire dans un emplacement de la structure de répertoire différent de l’objet de fichier ou de répertoire auquel il est lié.</span><span class="sxs-lookup"><span data-stu-id="c1fe0-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="c1fe0-105">Ce processus est appelé liaison.</span><span class="sxs-lookup"><span data-stu-id="c1fe0-105">This process is called linking.</span></span> <span data-ttu-id="c1fe0-106">Il existe deux types de liens pris en charge dans le système de fichiers NTFS : les [liens physiques et les jonctions](hard-links-and-junctions.md).</span><span class="sxs-lookup"><span data-stu-id="c1fe0-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="c1fe0-107">Le système de fichiers NTFS fournit également le [service de suivi de lien distribué](distributed-link-tracking-and-object-identifiers.md), qui assure le suivi automatique des liens à mesure qu’ils sont déplacés.</span><span class="sxs-lookup"><span data-stu-id="c1fe0-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1fe0-108">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c1fe0-108">In this section</span></span>



| <span data-ttu-id="c1fe0-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c1fe0-109">Topic</span></span>                                                                                                               | <span data-ttu-id="c1fe0-110">Description</span><span class="sxs-lookup"><span data-stu-id="c1fe0-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1fe0-111">Liens physiques et jonctions</span><span class="sxs-lookup"><span data-stu-id="c1fe0-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="c1fe0-112">Décrit les liens physiques et les jonctions.</span><span class="sxs-lookup"><span data-stu-id="c1fe0-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="c1fe0-113">Suivi des liaisons distribuées et identificateurs d’objets</span><span class="sxs-lookup"><span data-stu-id="c1fe0-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="c1fe0-114">Le **service de suivi de lien distribué** permet aux applications clientes de suivre les sources de liens qui ont été déplacées.</span><span class="sxs-lookup"><span data-stu-id="c1fe0-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




