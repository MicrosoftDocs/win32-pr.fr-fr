---
title: Contrôle de version et stratégies de secours
description: Quand une application détecte une mise à jour partielle à l’aide de l’une des techniques précédentes ou lit un ensemble d’objets dont la date d’effet n’a pas encore été atteinte, l’application doit gérer la situation de manière appropriée.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Contrôle de version et stratégies de secours AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839262"
---
# <a name="versioning-and-fallback-strategies"></a>Contrôle de version et stratégies de secours

Quand une application détecte une mise à jour partielle à l’aide de l’une des techniques précédentes ou lit un ensemble d’objets dont la date d’effet n’a pas encore été atteinte, l’application doit gérer la situation de manière appropriée. Pour certaines applications, la réponse normale consiste à « revenir » à une version précédente des objets en question. Active Directory Domain Services ne fournissez pas de fonctionnalité de contrôle de version, les applications qui souhaitent que cette fonctionnalité les fournisse eux-mêmes. Les approches de la gestion des versions incluent la conservation locale des valeurs « dernières bonnes connues » et le stockage de plusieurs ensembles d’objets dans l’annuaire, par exemple, dans les conteneurs « ancien », « actuel » et « nouveau ». De nombreux autres schémas sont possibles.

Les implémentations doivent veiller à éviter des conséquences inattendues. Une version antérieure d’objets doit être utilisée uniquement lorsqu’une mise à jour partielle est détectée ou que les nouveaux objets ne sont pas encore « effectifs ». En arrière-plan, car un événement de l’application « ne fonctionne pas » peut contourner l’intention d’un administrateur. Par exemple, deux ordinateurs qui pouvaient auparavant communiquer peuvent se trouver incapables de le faire en raison d’une modification de la stratégie IPsec (Internet Protocol Security). Si cela est intentionnel pour la part de l’administrateur, les systèmes affectés ne doivent pas revenir à la stratégie qui leur a permis de communiquer, car il s’agit d’une violation de la sécurité.

 

 




