---
title: Exemples d’extensions de classe d’assistance NDF
description: Ces exemples s’appliquent uniquement lorsque les développeurs pensent qu’il est nécessaire d’étendre les fonctionnalités d’une classe d’assistance Microsoft NDF déclarée comme étant extensible.
ms.assetid: 048e42f5-66d8-41c6-9e97-8da68c9ad151
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3ecf34bb8e90aad8c28f582860d44e81706e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670914"
---
# <a name="ndf-helper-class-extension-examples"></a><span data-ttu-id="95e49-103">Exemples d’extensions de classe d’assistance NDF</span><span class="sxs-lookup"><span data-stu-id="95e49-103">NDF Helper Class Extension Examples</span></span>

<span data-ttu-id="95e49-104">Ces exemples s’appliquent uniquement lorsque les développeurs pensent qu’il est nécessaire d’étendre les fonctionnalités d’une classe d’assistance Microsoft NDF déclarée comme étant extensible.</span><span class="sxs-lookup"><span data-stu-id="95e49-104">These examples apply only when developers believe it is necessary to extend the functionality of a Microsoft NDF Helper Class that is declared to be extensible.</span></span> <span data-ttu-id="95e49-105">Cela n’est généralement pas nécessaire, mais dans certains cas, des opportunités de diagnostic uniques se présentent elles-mêmes en raison de la configuration matérielle ou logicielle spécifique au composant.</span><span class="sxs-lookup"><span data-stu-id="95e49-105">This is generally not necessary, but in some cases, unique diagnostic opportunities present themselves because of the specific hardware or software requirements of the component.</span></span>

<span data-ttu-id="95e49-106">Les deux exemples suivants sont liés et la première doit être comprise avant d’analyser la seconde.</span><span class="sxs-lookup"><span data-stu-id="95e49-106">The two examples that follow are related and the first should be understood before analyzing the second.</span></span> <span data-ttu-id="95e49-107">La première fournit une implémentation d’une [extension de classe d’assistance NDF](ndf-helper-class-example.md) à l’aide d’une classe appelée SimpleHelperFileClass.</span><span class="sxs-lookup"><span data-stu-id="95e49-107">The first provides an implementation of an [NDF Helper Class Extension](ndf-helper-class-example.md) using a class called SimpleHelperFileClass.</span></span>

<span data-ttu-id="95e49-108">La deuxième [extension de classe d’assistance NDF avec la remise](ndf-helper-class-example-with-handoff.md), fournit un exemple d’extension qui n’effectue pas de tâches de diagnostic spécifiques, mais génère uniquement une hypothèse d’intégrité faible pour SimpleHelperFileClass dans le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="95e49-108">The second, [NDF Helper Class Extension with Handoff](ndf-helper-class-example-with-handoff.md), provides an example of an extension that does not perform specific diagnostic tasks but only generates a low health hypothesis for the SimpleHelperFileClass in the first example.</span></span>

 

 




