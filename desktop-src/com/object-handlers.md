---
title: Gestionnaires d’objets
description: Gestionnaires d’objets
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839529"
---
# <a name="object-handlers"></a><span data-ttu-id="68bfb-103">Gestionnaires d’objets</span><span class="sxs-lookup"><span data-stu-id="68bfb-103">Object Handlers</span></span>

<span data-ttu-id="68bfb-104">Si une application serveur OLE est un serveur local, ce qui signifie qu’elle s’exécute dans son propre espace de processus, la communication entre le conteneur et le serveur doit être effectuée au-delà des limites du processus.</span><span class="sxs-lookup"><span data-stu-id="68bfb-104">If an OLE server application is a local server, meaning that it runs in its own process space, communication between container and server must occur across process boundaries.</span></span> <span data-ttu-id="68bfb-105">Étant donné que ce processus est onéreux, OLE s’appuie sur un objet de substitution chargé dans l’espace de processus du conteneur pour agir pour le compte d’une application serveur locale.</span><span class="sxs-lookup"><span data-stu-id="68bfb-105">Because this process is expensive, OLE relies on a surrogate object loaded into the container's process space to act on behalf of a local server application.</span></span> <span data-ttu-id="68bfb-106">Cet objet de substitution, connu sous le nom de *Gestionnaire d’objets*, demande de conteneur de services qui ne requiert pas l’attention de l’application serveur, comme les demandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="68bfb-106">This surrogate object, known as an *object handler*, services container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="68bfb-107">Lorsqu’un conteneur demande un objet que le gestionnaire d’objets ne peut pas fournir, le gestionnaire communique avec l’application serveur à l’aide du mécanisme de communication out-of-process de COM.</span><span class="sxs-lookup"><span data-stu-id="68bfb-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using COM's out-of-process communication mechanism.</span></span>

<span data-ttu-id="68bfb-108">Un gestionnaire d’objets est unique à une classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="68bfb-108">An object handler is unique to an object class.</span></span> <span data-ttu-id="68bfb-109">Lorsque vous créez une instance d’un gestionnaire pour une classe, vous ne pouvez pas l’utiliser pour une autre.</span><span class="sxs-lookup"><span data-stu-id="68bfb-109">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="68bfb-110">Lorsqu’il est utilisé pour un document composé, le gestionnaire d’objets implémente les structures de données côté conteneur lorsque vous accédez aux objets d’une classe particulière à distance.</span><span class="sxs-lookup"><span data-stu-id="68bfb-110">When used for a compound document, the object handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="68bfb-111">OLE fournit un gestionnaire d’objets par défaut que les applications serveur locales peuvent utiliser.</span><span class="sxs-lookup"><span data-stu-id="68bfb-111">OLE provides a default object handler that local server applications can use.</span></span> <span data-ttu-id="68bfb-112">Pour les applications qui requièrent des comportements spéciaux, les développeurs peuvent implémenter un gestionnaire personnalisé qui remplace le gestionnaire par défaut ou l’utilise pour fournir certains comportements par défaut.</span><span class="sxs-lookup"><span data-stu-id="68bfb-112">For applications that require special behaviors, developers can implement a custom handler that either replaces the default handler or uses it to provide certain default behaviors.</span></span>

<span data-ttu-id="68bfb-113">Un gestionnaire d’objets est une DLL contenant plusieurs composants interactifs.</span><span class="sxs-lookup"><span data-stu-id="68bfb-113">An object handler is a DLL containing several interacting components.</span></span> <span data-ttu-id="68bfb-114">Ces composants incluent des éléments de communication à distance pour gérer la communication entre le gestionnaire et son application serveur, un cache pour le stockage des données d’un objet, ainsi que des informations sur la façon dont ces données doivent être mises en forme et affichées, ainsi qu’un objet de contrôle qui coordonne les activités des autres composants de la DLL.</span><span class="sxs-lookup"><span data-stu-id="68bfb-114">These components include remoting pieces to manage communication between the handler and its server application, a cache for storing an object's data, along with information on how that data should be formatted and displayed, and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="68bfb-115">En outre, si un objet est un lien, la DLL comprend également un composant de liaison, ou un *objet lié*, qui assure le suivi du nom et de l’emplacement de la source de la liaison.</span><span class="sxs-lookup"><span data-stu-id="68bfb-115">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="68bfb-116">Le *cache* contient des données et des informations de présentation suffisantes pour que le gestionnaire affiche un objet chargé, mais pas en cours d’exécution, dans son conteneur.</span><span class="sxs-lookup"><span data-stu-id="68bfb-116">The *cache* contains data and presentation information sufficient for the handler to display a loaded, but not running, object in its container.</span></span> <span data-ttu-id="68bfb-117">OLE fournit une implémentation du cache utilisé par le gestionnaire d’objets par défaut d’OLE et l’objet Link.</span><span class="sxs-lookup"><span data-stu-id="68bfb-117">OLE provides an implementation of the cache used by OLE's default object handler and the link object.</span></span> <span data-ttu-id="68bfb-118">Le cache stocke les données dans les formats requis par le gestionnaire d’objets pour répondre aux demandes de dessin de conteneur.</span><span class="sxs-lookup"><span data-stu-id="68bfb-118">The cache stores data in formats needed by the object handler to satisfy container draw requests.</span></span> <span data-ttu-id="68bfb-119">Lorsque les données d’un objet sont modifiées, l’objet envoie une notification au cache pour qu’une mise à jour puisse se produire.</span><span class="sxs-lookup"><span data-stu-id="68bfb-119">When an object's data changes, the object sends a notification to the cache so that an update can occur.</span></span> <span data-ttu-id="68bfb-120">Pour plus d’informations sur le cache, consultez [afficher la mise en cache](view-caching.md).</span><span class="sxs-lookup"><span data-stu-id="68bfb-120">For more information on the cache, see [View Caching](view-caching.md).</span></span>

<span data-ttu-id="68bfb-121">Pour plus d'informations, voir la rubrique suivante :</span><span class="sxs-lookup"><span data-stu-id="68bfb-121">For more information, see the following topic:</span></span>

-   [<span data-ttu-id="68bfb-122">Gestionnaire par défaut et gestionnaires personnalisés</span><span class="sxs-lookup"><span data-stu-id="68bfb-122">The Default Handler and Custom Handlers</span></span>](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="68bfb-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68bfb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68bfb-124">Documents composés</span><span class="sxs-lookup"><span data-stu-id="68bfb-124">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




