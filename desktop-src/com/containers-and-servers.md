---
title: Conteneurs et serveurs
description: Conteneurs et serveurs
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840789"
---
# <a name="containers-and-servers"></a><span data-ttu-id="e86bf-103">Conteneurs et serveurs</span><span class="sxs-lookup"><span data-stu-id="e86bf-103">Containers and Servers</span></span>

<span data-ttu-id="e86bf-104">Les applications de document composé sont de deux types de base : les applications de conteneur et les applications serveur.</span><span class="sxs-lookup"><span data-stu-id="e86bf-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="e86bf-105">Les applications de conteneur OLE fournissent aux utilisateurs la possibilité de créer, de modifier, d’enregistrer et de récupérer des documents composés.</span><span class="sxs-lookup"><span data-stu-id="e86bf-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="e86bf-106">Les applications serveur OLE fournissent aux utilisateurs les moyens de créer des documents et d’autres représentations de données qui peuvent être contenus comme des liens ou des incorporations dans les applications de conteneur.</span><span class="sxs-lookup"><span data-stu-id="e86bf-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="e86bf-107">Une application OLE peut être une application de conteneur, une application serveur, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e86bf-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="e86bf-108">Les applications serveur OLE varient également selon qu’elles sont implémentées en tant que *serveurs in-process* ou *serveurs locaux*.</span><span class="sxs-lookup"><span data-stu-id="e86bf-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="e86bf-109">Un serveur in-process est une bibliothèque de liens dynamiques (DLL) qui s’exécute dans l’espace de processus de l’application conteneur.</span><span class="sxs-lookup"><span data-stu-id="e86bf-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="e86bf-110">Vous ne pouvez exécuter un serveur in-process qu’à partir de l’application conteneur.</span><span class="sxs-lookup"><span data-stu-id="e86bf-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="e86bf-111">Les versions ultérieures d’OLE activent la liaison et l’incorporation à travers les limites de l’ordinateur, de sorte qu’une application de conteneur sur un ordinateur puisse utiliser un objet de document composé fourni par un *serveur distant* exécuté sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e86bf-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="e86bf-112">Du point de vue d’une application de conteneur, toute application serveur OLE qui s’exécute dans son propre espace de processus, que ce soit sur le même ordinateur ou sur un ordinateur distant, est un *serveur hors processÂ*.</span><span class="sxs-lookup"><span data-stu-id="e86bf-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e86bf-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e86bf-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86bf-114">Documents composés</span><span class="sxs-lookup"><span data-stu-id="e86bf-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="e86bf-115">Serveurs in-process</span><span class="sxs-lookup"><span data-stu-id="e86bf-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




