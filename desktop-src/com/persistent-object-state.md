---
title: État persistant de l’objet
description: État persistant de l’objet
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309530"
---
# <a name="persistent-object-state"></a><span data-ttu-id="846f8-103">État persistant de l’objet</span><span class="sxs-lookup"><span data-stu-id="846f8-103">Persistent Object State</span></span>

<span data-ttu-id="846f8-104">Certains objets COM peuvent enregistrer leur état interne lorsqu’un client le leur demande.</span><span class="sxs-lookup"><span data-stu-id="846f8-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="846f8-105">COM définit les normes par le biais desquelles les clients peuvent demander l’initialisation, le chargement et l’enregistrement d’objets dans un magasin de données (par exemple, un fichier plat, un stockage structuré ou la mémoire).</span><span class="sxs-lookup"><span data-stu-id="846f8-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="846f8-106">Il incombe au client de gérer l’emplacement où les données persistantes de l’objet sont stockées, mais pas le format des données.</span><span class="sxs-lookup"><span data-stu-id="846f8-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="846f8-107">Les objets COM qui adhèrent à ces normes sont appelés *objets persistants*.</span><span class="sxs-lookup"><span data-stu-id="846f8-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="846f8-108">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="846f8-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="846f8-109">Interfaces d’objets persistants</span><span class="sxs-lookup"><span data-stu-id="846f8-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="846f8-110">Initialisation d’objets persistants</span><span class="sxs-lookup"><span data-stu-id="846f8-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="846f8-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="846f8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="846f8-112">Clients et serveurs COM</span><span class="sxs-lookup"><span data-stu-id="846f8-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




