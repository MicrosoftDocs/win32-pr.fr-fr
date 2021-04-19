---
description: Le SCM prend en charge les types de handle pour autoriser l’accès aux objets suivants.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: Handles SCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544320"
---
# <a name="scm-handles"></a><span data-ttu-id="2fb36-103">Handles SCM</span><span class="sxs-lookup"><span data-stu-id="2fb36-103">SCM Handles</span></span>

<span data-ttu-id="2fb36-104">Le SCM prend en charge les types de handle pour autoriser l’accès aux objets suivants.</span><span class="sxs-lookup"><span data-stu-id="2fb36-104">The SCM supports handle types to allow access to the following objects.</span></span>

-   <span data-ttu-id="2fb36-105">Base de données des services installés.</span><span class="sxs-lookup"><span data-stu-id="2fb36-105">The database of installed services.</span></span>
-   <span data-ttu-id="2fb36-106">Service.</span><span class="sxs-lookup"><span data-stu-id="2fb36-106">A service.</span></span>
-   <span data-ttu-id="2fb36-107">Verrou de base de données.</span><span class="sxs-lookup"><span data-stu-id="2fb36-107">The database lock.</span></span>

<span data-ttu-id="2fb36-108">Un objet SCManager représente la base de données de services installés.</span><span class="sxs-lookup"><span data-stu-id="2fb36-108">An SCManager object represents the database of installed services.</span></span> <span data-ttu-id="2fb36-109">Il s’agit d’un objet conteneur qui contient des objets de service.</span><span class="sxs-lookup"><span data-stu-id="2fb36-109">It is a container object that holds service objects.</span></span> <span data-ttu-id="2fb36-110">La fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) retourne un handle à un objet SCManager sur un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2fb36-110">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function returns a handle to an SCManager object on a specified computer.</span></span> <span data-ttu-id="2fb36-111">Ce descripteur est utilisé lors de l’installation, de la suppression, de l’ouverture et de l’énumération des services et du verrouillage de la base de données de services.</span><span class="sxs-lookup"><span data-stu-id="2fb36-111">This handle is used when installing, deleting, opening, and enumerating services and when locking the services database.</span></span>

<span data-ttu-id="2fb36-112">Un objet de service représente un service installé.</span><span class="sxs-lookup"><span data-stu-id="2fb36-112">A service object represents an installed service.</span></span> <span data-ttu-id="2fb36-113">Les fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) retournent des handles aux services installés.</span><span class="sxs-lookup"><span data-stu-id="2fb36-113">The [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions return handles to installed services.</span></span>

<span data-ttu-id="2fb36-114">Les fonctions [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)et [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) peuvent demander différents types d’accès aux SCManager et aux objets de service.</span><span class="sxs-lookup"><span data-stu-id="2fb36-114">The [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera), [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea), and [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) functions can request different types of access to SCManager and service objects.</span></span> <span data-ttu-id="2fb36-115">L’accès demandé est accordé ou refusé en fonction du jeton d’accès du processus appelant et du descripteur de sécurité associé à l’objet de service ou SCManager.</span><span class="sxs-lookup"><span data-stu-id="2fb36-115">The requested access is granted or denied depending on the access token of the calling process and the security descriptor associated with the SCManager or service object.</span></span>

<span data-ttu-id="2fb36-116">La fonction [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) ferme les handles des objets SCManager et service.</span><span class="sxs-lookup"><span data-stu-id="2fb36-116">The [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) function closes handles to SCManager and service objects.</span></span> <span data-ttu-id="2fb36-117">Lorsque vous n’avez plus besoin de ces handles, veillez à les fermer.</span><span class="sxs-lookup"><span data-stu-id="2fb36-117">When you no longer need these handles, be sure to close them.</span></span>

 

 



