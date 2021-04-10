---
description: Le système utilise des objets et des handles pour réguler l’accès aux ressources système pour deux raisons principales.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: À propos des handles et des objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952101"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="1d52b-103">À propos des handles et des objets</span><span class="sxs-lookup"><span data-stu-id="1d52b-103">About Handles and Objects</span></span>

<span data-ttu-id="1d52b-104">Le système utilise des objets et des handles pour réguler l’accès aux ressources système pour deux raisons principales.</span><span class="sxs-lookup"><span data-stu-id="1d52b-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="1d52b-105">Tout d’abord, l’utilisation des objets garantit que Microsoft peut mettre à jour les fonctionnalités du système, tant que l’interface d’objet d’origine est conservée.</span><span class="sxs-lookup"><span data-stu-id="1d52b-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="1d52b-106">Lorsque des versions ultérieures du système sont publiées, vous pouvez utiliser l’objet mis à jour avec peu ou pas de travail supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1d52b-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="1d52b-107">Deuxièmement, l’utilisation d’objets vous permet de tirer parti de la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="1d52b-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="1d52b-108">Chaque objet possède sa propre liste de contrôle d’accès (ACL) qui spécifie les actions qu’un processus peut effectuer sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d52b-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="1d52b-109">Le système examine l’ACL d’un objet chaque fois qu’une application crée un handle pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d52b-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="1d52b-110">Pour obtenir plus d'informations, voir [Contrôle d'accès](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="1d52b-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="1d52b-111">Gestionnaire d’objets</span><span class="sxs-lookup"><span data-stu-id="1d52b-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="1d52b-112">Interface d’objet</span><span class="sxs-lookup"><span data-stu-id="1d52b-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="1d52b-113">Espaces de noms d’objets</span><span class="sxs-lookup"><span data-stu-id="1d52b-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="1d52b-114">Limitations des handles</span><span class="sxs-lookup"><span data-stu-id="1d52b-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="1d52b-115">Gérer l’héritage</span><span class="sxs-lookup"><span data-stu-id="1d52b-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
