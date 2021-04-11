---
title: Inscription des applications COM
description: Inscription des applications COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310945"
---
# <a name="registering-com-applications"></a><span data-ttu-id="14606-103">Inscription des applications COM</span><span class="sxs-lookup"><span data-stu-id="14606-103">Registering COM Applications</span></span>

<span data-ttu-id="14606-104">Le Registre est une base de données système qui contient des informations sur la configuration du matériel et des logiciels du système, ainsi que sur les utilisateurs du système.</span><span class="sxs-lookup"><span data-stu-id="14606-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="14606-105">N’importe quel programme Windows peut ajouter des informations au registre et lire des informations à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="14606-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="14606-106">Les clients recherchent dans le registre des composants intéressants à utiliser.</span><span class="sxs-lookup"><span data-stu-id="14606-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="14606-107">Le registre contient des informations sur tous les objets COM installés dans le système.</span><span class="sxs-lookup"><span data-stu-id="14606-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="14606-108">Chaque fois qu’une application crée une instance d’un composant COM, le Registre est consulté pour résoudre le CLSID ou le ProgID du composant dans le chemin d’accès de la DLL du serveur ou de l’EXE qui le contient.</span><span class="sxs-lookup"><span data-stu-id="14606-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="14606-109">Une fois le serveur du composant déterminé, Windows charge le serveur dans l’espace de processus de l’application cliente (composants in-process) ou démarre le serveur dans son propre espace de processus (serveurs locaux et distants).</span><span class="sxs-lookup"><span data-stu-id="14606-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="14606-110">Le serveur crée une instance du composant et retourne au client une référence à l’une des interfaces du composant.</span><span class="sxs-lookup"><span data-stu-id="14606-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="14606-111">Pour plus d’informations sur le Registre Windows, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="14606-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="14606-112">Hiérarchie du Registre</span><span class="sxs-lookup"><span data-stu-id="14606-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="14606-113">Classes et serveurs</span><span class="sxs-lookup"><span data-stu-id="14606-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="14606-114">Classification des composants</span><span class="sxs-lookup"><span data-stu-id="14606-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="14606-115">Utilisation d’OleView</span><span class="sxs-lookup"><span data-stu-id="14606-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="14606-116">Inscription des composants</span><span class="sxs-lookup"><span data-stu-id="14606-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="14606-117">Vérification de l’inscription</span><span class="sxs-lookup"><span data-stu-id="14606-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="14606-118">Types d’utilisateurs inconnus</span><span class="sxs-lookup"><span data-stu-id="14606-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="14606-119">Clés de registre COM</span><span class="sxs-lookup"><span data-stu-id="14606-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 




