---
description: L’illustration suivante montre comment deux applications peuvent partager un assembly à l’aide de la méthode traditionnelle de partage d’assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Partage d’assembly côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952799"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="da699-103">Partage d’assembly côte à côte</span><span class="sxs-lookup"><span data-stu-id="da699-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="da699-104">L’illustration suivante montre comment deux applications peuvent partager un assembly à l’aide de la méthode traditionnelle de partage d’assembly.</span><span class="sxs-lookup"><span data-stu-id="da699-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="da699-105">Un problème de partage d’assembly traditionnel se produit lorsqu’une application installe une version d’un assembly (généralement une DLL) qui n’est pas à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="da699-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="da699-106">L’application qui vient d’être installée fonctionne, mais les applications qui dépendent de la version précédente de la DLL risquent de ne plus fonctionner.</span><span class="sxs-lookup"><span data-stu-id="da699-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![représentation de deux applications partageant un assembly](images/sxs1.png)

<span data-ttu-id="da699-108">L’application isolée et la solution d’assembly côte à côte permettent à différentes versions du même assembly Win32 de s’exécuter en même temps sur le même système sans conflit.</span><span class="sxs-lookup"><span data-stu-id="da699-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="da699-109">En spécifiant la version d’assembly côte à côte que l’application doit utiliser, les développeurs peuvent garantir que la configuration testée sera toujours dupliquée sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da699-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="da699-110">Le partage côte à côte est illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="da699-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![implémentation du partage d’assembly côte à côte](images/sxs2.png)

<span data-ttu-id="da699-112">Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="da699-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



