---
description: Un lien symbolique est un objet de système de fichiers qui pointe vers un autre objet de système de fichiers. L’objet désigné est appelé la cible.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Liens symboliques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545045"
---
# <a name="symbolic-links"></a><span data-ttu-id="37bf9-104">Liens symboliques</span><span class="sxs-lookup"><span data-stu-id="37bf9-104">Symbolic Links</span></span>

<span data-ttu-id="37bf9-105">Un lien symbolique est un objet de système de fichiers qui pointe vers un autre objet de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="37bf9-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="37bf9-106">L’objet désigné est appelé la cible.</span><span class="sxs-lookup"><span data-stu-id="37bf9-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="37bf9-107">Les liens symboliques sont transparents pour les utilisateurs ; les liens apparaissent en tant que fichiers ou répertoires normaux et peuvent être traités par l’utilisateur ou l’application exactement de la même manière.</span><span class="sxs-lookup"><span data-stu-id="37bf9-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="37bf9-108">Les liens symboliques sont conçus pour faciliter la migration et la compatibilité des applications avec les systèmes d’exploitation UNIX.</span><span class="sxs-lookup"><span data-stu-id="37bf9-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="37bf9-109">Microsoft a implémenté ses liens symboliques pour fonctionner comme des liens UNIX.</span><span class="sxs-lookup"><span data-stu-id="37bf9-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="37bf9-110">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="37bf9-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37bf9-111">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="37bf9-111">In this section</span></span>



| <span data-ttu-id="37bf9-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="37bf9-112">Topic</span></span>                                                                                                             | <span data-ttu-id="37bf9-113">Description</span><span class="sxs-lookup"><span data-stu-id="37bf9-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37bf9-114">Effets de liens symboliques sur les fonctions des systèmes de fichiers</span><span class="sxs-lookup"><span data-stu-id="37bf9-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="37bf9-115">La façon dont les liens symboliques affectent les fonctions de fichier standard qui utilisent des noms de chemin d’accès pour spécifier un ou plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="37bf9-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="37bf9-116">Considérations relatives à la programmation</span><span class="sxs-lookup"><span data-stu-id="37bf9-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="37bf9-117">Considérations relatives à la programmation pour l’utilisation des liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="37bf9-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="37bf9-118">Création de liens symboliques</span><span class="sxs-lookup"><span data-stu-id="37bf9-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="37bf9-119">Créez des liens symboliques qui utilisent un chemin d’accès absolu ou relatif à l’aide de la fonction [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .</span><span class="sxs-lookup"><span data-stu-id="37bf9-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="37bf9-120">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bf9-120">Supported Operating Systems</span></span>

<span data-ttu-id="37bf9-121">Les liens symboliques sont disponibles dans NTFS à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37bf9-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




