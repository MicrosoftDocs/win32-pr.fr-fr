---
description: Les modules de fusion requièrent rarement une interface utilisateur.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Création d’interfaces utilisateur dans les modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517662"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="49139-103">Création d’interfaces utilisateur dans les modules de fusion</span><span class="sxs-lookup"><span data-stu-id="49139-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="49139-104">Les modules de fusion requièrent rarement une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49139-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="49139-105">La libération d’un module de fusion qui contient à la fois des composants installables et une interface utilisateur restreint finalement la flexibilité de l’utilisateur du module.</span><span class="sxs-lookup"><span data-stu-id="49139-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="49139-106">La combinaison des composants et de l’interface utilisateur dans un seul module peut empêcher les développeurs d’utiliser leur propre interface utilisateur ou de fournir des installations en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="49139-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="49139-107">Une meilleure solution consiste à libérer deux modules de fusion, un qui installe silencieusement les composants et un second module facultatif qui contient l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49139-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="49139-108">Le module avec l’interface utilisateur doit répertorier le module de composant dans sa [table ModuleDependency](moduledependency-table.md).</span><span class="sxs-lookup"><span data-stu-id="49139-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="49139-109">Cette méthode permet aux auteurs de module de fournir une interface utilisateur sans l’imposer aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="49139-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="49139-110">Lorsque des tables d’interface utilisateur sont utilisées dans des modules de fusion, elles peuvent être fusionnées de la même façon que les autres tables.</span><span class="sxs-lookup"><span data-stu-id="49139-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 



