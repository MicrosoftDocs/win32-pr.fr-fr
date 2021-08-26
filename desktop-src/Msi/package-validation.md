---
description: Il est fortement recommandé d’exécuter la validation sur chaque package d’installation nouveau ou récemment modifié avant d’essayer d’installer le package pour la première fois.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validations de package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2fb8fe877f68a1c787458e7703fb59f035031fc68bba1d75f24e86851aac7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074849"
---
# <a name="package-validation"></a>Validations de package

Il est fortement recommandé d’exécuter la validation sur chaque package d’installation nouveau ou récemment modifié avant d’essayer d’installer le package pour la première fois.

La validation de package comprend les trois processus suivants :

-   [Validation interne](internal-validation.md)
-   [Validation du pool de chaînes](string-pool-validation.md)
-   [Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)

Les modules de fusion doivent être validés à l’aide de la méthode décrite dans [validation des modules de fusion](validating-merge-modules.md).

Evalcom2.dll fournit un objet COM qui implémente les opérations de validation des packages d’installation et des modules de fusion. L’objet principal implémente des interfaces pour les programmes C/C++. Pour plus d’informations, consultez [Automation de validation](validation-automation.md).

 

 



