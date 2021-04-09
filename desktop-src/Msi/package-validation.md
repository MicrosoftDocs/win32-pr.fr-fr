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
# <a name="package-validation"></a>Validations de package

Il est fortement recommandé d’exécuter la validation sur chaque package d’installation nouveau ou récemment modifié avant d’essayer d’installer le package pour la première fois.

La validation de package comprend les trois processus suivants :

-   [Validation interne](internal-validation.md)
-   [Validation du pool de chaînes](string-pool-validation.md)
-   [Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)

Les modules de fusion doivent être validés à l’aide de la méthode décrite dans [validation des modules de fusion](validating-merge-modules.md).

Evalcom2.dll fournit un objet COM qui implémente les opérations de validation des packages d’installation et des modules de fusion. L’objet principal implémente des interfaces pour les programmes C/C++. Pour plus d’informations, consultez [Automation de validation](validation-automation.md).

 

 



