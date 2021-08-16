---
description: Services COM+ sans composants
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Services COM+ sans composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b395186875c37fb42e5011ee0486aa6de86ffe62b73c8ea1a54c09e82a27c588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638449"
---
# <a name="com-services-without-components"></a>Services COM+ sans composants

Avec COM+ 1,5, vous pouvez utiliser les services fournis par COM+ sans avoir à créer un composant pour contenir les méthodes qui appellent ces services. Cela permet aux développeurs qui n’utilisent pas généralement des composants d’utiliser des services COM+ tels que des transactions ou le dispositif de suivi COM+. En utilisant des services COM+ sans composants, les développeurs peuvent éviter la surcharge liée à la création d’un composant qui est utilisé pour accéder uniquement aux services COM+ dont ils ont besoin.

Par exemple, les environnements de script ont traditionnellement été les plus grands consommateurs de services COM+, mais ils n’ont jamais pu utiliser ces services efficacement parce que les services devaient être regroupés dans un composant COM+. Cette exigence de regroupement a augmenté les coûts de performances en raison de l’augmentation de la communication et de la duplication des données nécessaires à l’environnement de script pour interagir avec le composant. En utilisant des services sans composants, ces coûts sont réduits.

Les rubriques décrites dans le tableau suivant fournissent des informations générales et sur les tâches relatives à l’utilisation des services COM+ sans composants. Cette fonctionnalité est destinée aux développeurs avancés Visual C++ qui se soucient des performances.



| Rubrique                                                                                                 | Description                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Concepts des services COM+ sans composants](com--services-without-components-concepts.md)<br/> | Fournit une vue d’ensemble de l’utilisation des services COM+ sans composants.<br/>                     |
| [Tâches des services COM+ sans composants](com--services-without-components-tasks.md)<br/>       | Fournit des instructions sur l’utilisation de COM+ pour créer et utiliser des services sans composants.<br/> |



 

 

 




