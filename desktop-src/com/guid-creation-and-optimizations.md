---
title: Création et optimisations de GUID
description: Création et optimisations de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380339"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="a08f6-103">Création et optimisations de GUID</span><span class="sxs-lookup"><span data-stu-id="a08f6-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="a08f6-104">Comme un CLSID, comme un identificateur d’interface (IID), est un GUID, aucune autre classe, quelle que soit la personne qui l’écrit, a un CLSID en double.</span><span class="sxs-lookup"><span data-stu-id="a08f6-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="a08f6-105">Les implémenteurs de serveur obtiennent généralement des CLSID par le biais de la fonction [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .</span><span class="sxs-lookup"><span data-stu-id="a08f6-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="a08f6-106">Cette fonction est assurée pour produire des CLSID uniques, de sorte que les responsables de l’implémentation de serveur dans le monde entier peuvent développer et déployer leurs logiciels indépendamment sans crainte de collision accidentelle avec les logiciels écrits par d’autres.</span><span class="sxs-lookup"><span data-stu-id="a08f6-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="a08f6-107">L’utilisation de CLSID uniques évite le risque de collisions de noms entre les classes, car les CLSID ne sont en aucun cas connectés aux noms utilisés dans l’implémentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="a08f6-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="a08f6-108">Par exemple, deux fournisseurs différents peuvent écrire des classes appelées « StackClass », mais chacun a un CLSID unique et n’a donc pas pu être confondu.</span><span class="sxs-lookup"><span data-stu-id="a08f6-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="a08f6-109">COM doit fréquemment mapper les GUID (IID et CLSID) à un ensemble arbitrairement important d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="a08f6-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="a08f6-110">En tant que développeur d’applications, vous pouvez accélérer ces recherches et améliorer ainsi les performances du système en générant les GUID de votre application sous la forme d’un bloc de valeurs consécutives.</span><span class="sxs-lookup"><span data-stu-id="a08f6-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="a08f6-111">La méthode la plus efficace pour générer un bloc de GUID consécutifs consiste à exécuter l’utilitaire uuidgen à l’aide des commutateurs-n et-x, qui génèrent un bloc d’UUID, chacun d’entre eux dont la première valeur DWORD est incrémentée d’une unité.</span><span class="sxs-lookup"><span data-stu-id="a08f6-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="a08f6-112">Par exemple, si vous tapez</span><span class="sxs-lookup"><span data-stu-id="a08f6-112">For example, if you were to type</span></span>

<span data-ttu-id="a08f6-113">**uuidgen-n5-x**</span><span class="sxs-lookup"><span data-stu-id="a08f6-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="a08f6-114">l’utilitaire uuidgen génère un bloc d’UUID similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="a08f6-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="a08f6-115">L’une des méthodes permettant de générer et de suivre des GUID pour un projet entier commence par la génération d’un bloc de plusieurs UUID, par exemple, 500.</span><span class="sxs-lookup"><span data-stu-id="a08f6-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="a08f6-116">Par exemple, si vous tapez</span><span class="sxs-lookup"><span data-stu-id="a08f6-116">For example, if you were to type</span></span>

<span data-ttu-id="a08f6-117">**uuidgen-N500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="a08f6-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="a08f6-118">l’utilitaire génère 500 UUID consécutifs et les écrit dans le fichier texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="a08f6-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="a08f6-119">Vous pouvez ensuite vérifier ce fichier dans votre arborescence source, en fournissant un référentiel unique pour tous les GUID à utiliser dans un projet.</span><span class="sxs-lookup"><span data-stu-id="a08f6-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="a08f6-120">À mesure que les utilisateurs ont besoin de GUID pour leurs parties du projet, ils peuvent extraire le fichier, prendre en compte de nombreux GUID dont ils ont besoin, les marquer comme pris et laisser une note sur l’emplacement du code ou « spec » qu’ils utilisent.</span><span class="sxs-lookup"><span data-stu-id="a08f6-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="a08f6-121">Outre l’amélioration des performances du système, la génération de blocs de GUID consécutifs de cette façon présente les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="a08f6-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="a08f6-122">Un fichier central contenant tous les GUID d’une application facilite le suivi des GUID qui sont destinés aux personnes qui les utilisent.</span><span class="sxs-lookup"><span data-stu-id="a08f6-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="a08f6-123">Un bloc de GUID consécutifs associés à une application particulière permet aux développeurs et aux testeurs de reconnaître les GUID internes lors du débogage et facilite leur recherche dans le registre système, car ils sont stockés de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="a08f6-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a08f6-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a08f6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a08f6-125">Responsabilités du serveur COM</span><span class="sxs-lookup"><span data-stu-id="a08f6-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




