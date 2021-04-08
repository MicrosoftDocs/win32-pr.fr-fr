---
description: Chaque assembly côte à côte doit avoir une version.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versions d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757317"
---
# <a name="assembly-versions"></a><span data-ttu-id="12478-103">Versions d’assembly</span><span class="sxs-lookup"><span data-stu-id="12478-103">Assembly Versions</span></span>

<span data-ttu-id="12478-104">Chaque assembly côte à côte doit avoir une version.</span><span class="sxs-lookup"><span data-stu-id="12478-104">Every side-by-side assembly must have a version.</span></span> <span data-ttu-id="12478-105">Chaque version d’assembly est associée à un numéro de version comportant quatre parties séparées par des points : *major. minor. Build. Revision*.</span><span class="sxs-lookup"><span data-stu-id="12478-105">Each assembly version is associated with a version number having four parts separated by periods: *major.minor.build.revision*.</span></span> <span data-ttu-id="12478-106">Si une modification est apportée à un assembly qui le rend incompatible avec les versions existantes, les parties *majeures* ou *secondaires* du numéro de version doivent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="12478-106">If a change is made to an assembly making it incompatible with existing versions, the *major* or *minor* parts of the version number must be changed.</span></span> <span data-ttu-id="12478-107">Un numéro de version qui change uniquement dans les parties de *Build* ou de *révision* indique que l’assembly est à compatibilité descendante avec les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="12478-107">A version number that changes only in the *build* or *revision* parts indicates that the assembly is backward compatible with prior versions.</span></span>

<span data-ttu-id="12478-108">La version doit être spécifiée dans les éléments **assemblyIdentity** des [manifestes](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="12478-108">The version must be specified in **assemblyIdentity** elements of [manifests](manifests.md).</span></span> <span data-ttu-id="12478-109">Utilisez le format de version en quatre parties : MMMM. nnnnn. ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="12478-109">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="12478-110">Chacun des composants séparés par des points peut être de 0-65535 inclus.</span><span class="sxs-lookup"><span data-stu-id="12478-110">Each of the parts separated by periods can be 0-65535 inclusive.</span></span>

 

 



