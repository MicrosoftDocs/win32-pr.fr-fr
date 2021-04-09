---
description: Il est fortement recommandé d’exécuter la validation sur chaque package d’installation nouveau ou récemment modifié avant d’essayer d’installer le package pour la première fois.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validations de package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864081"
---
# <a name="package-validation"></a><span data-ttu-id="b4386-103">Validations de package</span><span class="sxs-lookup"><span data-stu-id="b4386-103">Package Validation</span></span>

<span data-ttu-id="b4386-104">Il est fortement recommandé d’exécuter la validation sur chaque package d’installation nouveau ou récemment modifié avant d’essayer d’installer le package pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="b4386-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="b4386-105">La validation de package comprend les trois processus suivants :</span><span class="sxs-lookup"><span data-stu-id="b4386-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="b4386-106">Validation interne</span><span class="sxs-lookup"><span data-stu-id="b4386-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="b4386-107">Validation du pool de chaînes</span><span class="sxs-lookup"><span data-stu-id="b4386-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="b4386-108">Évaluateurs de cohérence internes-CIEM</span><span class="sxs-lookup"><span data-stu-id="b4386-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="b4386-109">Les modules de fusion doivent être validés à l’aide de la méthode décrite dans [validation des modules de fusion](validating-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="b4386-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="b4386-110">Evalcom2.dll fournit un objet COM qui implémente les opérations de validation des packages d’installation et des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="b4386-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="b4386-111">L’objet principal implémente des interfaces pour les programmes C/C++.</span><span class="sxs-lookup"><span data-stu-id="b4386-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="b4386-112">Pour plus d’informations, consultez [Automation de validation](validation-automation.md).</span><span class="sxs-lookup"><span data-stu-id="b4386-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 



