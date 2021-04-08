---
title: Utilisation de la constante prédéfinie __midl
description: Lorsque le compilateur MIDL traite les fichiers IDL et ACF d’entrée, \_ \_ MIDL est défini par défaut et est utilisé pour la compilation conditionnelle afin d’atteindre la cohérence dans l’ensemble de la génération.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL MIDL du compilateur MIDL, à l’aide de la constante prédéfinie _midl
- _midl MIDL de constante prédéfinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029287"
---
# <a name="using-the-__midl-predefined-constant"></a><span data-ttu-id="2a208-105">Utilisation de la \_ \_ constante prédéfinie MIDL</span><span class="sxs-lookup"><span data-stu-id="2a208-105">Using the \_\_midl Predefined Constant</span></span>

<span data-ttu-id="2a208-106">Lorsque le compilateur MIDL traite les fichiers IDL et ACF d’entrée, \_ \_ MIDL est défini par défaut et est utilisé pour la compilation conditionnelle afin d’atteindre la cohérence dans l’ensemble de la génération.</span><span class="sxs-lookup"><span data-stu-id="2a208-106">When the MIDL compiler processes the input IDL and ACF files, \_\_midl is defined by default and is used for conditional compilation to attain consistency throughout the build.</span></span> <span data-ttu-id="2a208-107">Cela permet d’extraire l’utilisation d’instructions de définition dans les fichiers d’en-tête, telles que **MIDL \_ Pass**, et de les remplacer par un indicateur cohérent.</span><span class="sxs-lookup"><span data-stu-id="2a208-107">This phases out the use of define statements in the header files, such as **MIDL\_PASS**, and replaces them with a consistent flag.</span></span> <span data-ttu-id="2a208-108">La valeur de la \_ \_ constante MIDL indique la version du compilateur *major. minor* en fonction de la formule *principale* \* 100 + *Minor*; par exemple, MIDL ver.</span><span class="sxs-lookup"><span data-stu-id="2a208-108">The value of the \_\_midl constant indicates the compiler version *major.minor* according to the formula *major* \* 100 + *minor*; for example MIDL ver.</span></span> <span data-ttu-id="2a208-109">6.0. x a le \_ \_ MIDL défini en tant que 600.</span><span class="sxs-lookup"><span data-stu-id="2a208-109">6.0.x has the \_\_midl defined as 600.</span></span>

<span data-ttu-id="2a208-110">Si vous le souhaitez, vous pouvez remplacer cette valeur par défaut en spécifiant les éléments suivants sur la ligne de commande : **/u \_ \_ MIDL**.</span><span class="sxs-lookup"><span data-stu-id="2a208-110">If you choose, you can override this default by specifying the following on the command line: **/U\_\_midl**.</span></span> <span data-ttu-id="2a208-111">Pour plus d’informations, consultez [**/u**](-u.md).</span><span class="sxs-lookup"><span data-stu-id="2a208-111">For more information, see [**/U**](-u.md).</span></span>

 

 




