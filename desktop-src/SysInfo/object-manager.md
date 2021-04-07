---
description: Un objet se compose d’un en-tête standard et d’attributs spécifiques à l’objet. Étant donné que tous les objets ont la même structure, il existe un seul gestionnaire d’objets dans Windows qui gère tous les objets.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gestionnaire d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952491"
---
# <a name="object-manager"></a><span data-ttu-id="aacae-104">Gestionnaire d’objets</span><span class="sxs-lookup"><span data-stu-id="aacae-104">Object Manager</span></span>

<span data-ttu-id="aacae-105">Un objet se compose d’un en-tête standard et d’attributs spécifiques à l’objet.</span><span class="sxs-lookup"><span data-stu-id="aacae-105">An object consists of a standard header and object-specific attributes.</span></span> <span data-ttu-id="aacae-106">Étant donné que tous les objets ont la même structure, il existe un seul gestionnaire d’objets dans Windows qui gère tous les objets.</span><span class="sxs-lookup"><span data-stu-id="aacae-106">Because all objects have the same structure, there is a single object manager in Windows that maintains all objects.</span></span>

<span data-ttu-id="aacae-107">L’en-tête d’objet comprend des éléments tels que le nom de l’objet, afin que d’autres processus puissent faire référence à l’objet par son nom et un descripteur de sécurité, afin que le gestionnaire d’objets puisse contrôler les processus qui accèdent à la ressource système.</span><span class="sxs-lookup"><span data-stu-id="aacae-107">The object header includes items such as the object name, so that other processes can reference the object by name, and a security descriptor, so that the object manager can control which processes access the system resource.</span></span>

<span data-ttu-id="aacae-108">Les tâches exécutées par le gestionnaire d’objets sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="aacae-108">The tasks that the object manager performs include the following:</span></span>

-   <span data-ttu-id="aacae-109">Création d'objets</span><span class="sxs-lookup"><span data-stu-id="aacae-109">Creating objects</span></span>
-   <span data-ttu-id="aacae-110">Vérification qu’un processus a le droit d’utiliser l’objet</span><span class="sxs-lookup"><span data-stu-id="aacae-110">Verifying that a process has the right to use the object</span></span>
-   <span data-ttu-id="aacae-111">Création de handles d’objet et retour à l’appelant</span><span class="sxs-lookup"><span data-stu-id="aacae-111">Creating object handles and returning them to the caller</span></span>
-   <span data-ttu-id="aacae-112">Gestion des quotas de ressources</span><span class="sxs-lookup"><span data-stu-id="aacae-112">Maintaining resource quotas</span></span>
-   <span data-ttu-id="aacae-113">Création de descripteurs dupliqués</span><span class="sxs-lookup"><span data-stu-id="aacae-113">Creating duplicate handles</span></span>
-   <span data-ttu-id="aacae-114">Fermeture des handles aux objets</span><span class="sxs-lookup"><span data-stu-id="aacae-114">Closing handles to objects</span></span>

 

 



