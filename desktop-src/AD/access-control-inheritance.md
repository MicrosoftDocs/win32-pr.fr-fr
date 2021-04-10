---
title: Héritage de Access Control
description: Les entrées de contrôle d’accès (ACE) dans une liste de contrôle d’accès (ACL) d’objet peuvent appartenir à une ACL effective ou hériter d’une ACL.
ms.assetid: 2530eef5-7804-4b27-8756-d97be1cea116
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec7514ab8cae8b07121d84e579ccb8492b67c45
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101401"
---
# <a name="access-control-inheritance"></a>Héritage de Access Control

Les entrées de contrôle d’accès (ACE) dans une liste de contrôle d’accès (ACL) d’objet peuvent appartenir à l’une des deux catégories suivantes :

-   ACL effective : les entrées de contrôle d’accès de cette catégorie s’appliquent à l’objet.
-   Hériter de l’ACL : les entrées de contrôle d’accès de cette catégorie sont héritées par les objets créés dans le conteneur.

Chaque entrée du contrôle d’accès de la liste DACL peut appartenir à une ou plusieurs catégories. Les catégories pour lesquelles un ACE appartient sont déterminées par les indicateurs de contrôle d’héritage définis dans l’entrée du contrôle d’accès.

Trois indicateurs de contrôle d’héritage peuvent être définis dans la propriété [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) d’une entrée du contrôle d’accès.



| Indicateur                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ACE ACEFLAG \_ hériter des publicités \_**                | Cet indicateur indique que l’entrée du contrôle d’accès fait partie de l’ACL inherit et que les objets enfants héritent des indicateurs de contrôle d’héritage de cette entrée du contrôle d’accès.                                                                                                                                                                                                                                                                                                                         |
| **AD \_ ACEFLAG \_ non \_ propager \_ hériter \_ ACE** | Cet indicateur indique que l’entrée du contrôle d’accès fait partie de l’ACL Inherit, mais qu’aucun indicateur de contrôle d’héritage n’est propagé aux objets enfants directs (descendants directs) et que l’entrée du contrôle d’accès est effective sur les objets enfants directs.                                                                                                                                                                                                                                          |
| **\_ACEFLAG ADS \_ hériter \_ uniquement \_ ACE**          | Cet indicateur indique que l’ACE ne fait pas partie d’une liste de contrôle d’accès effective. Si cet indicateur n’est pas défini, l’ACE fait partie de la liste de contrôle d’accès effective. Cet indicateur est utile pour définir des autorisations pouvant être héritées par des sous-objets, mais qui n’affectent pas l’accessibilité du conteneur. Par exemple, si un ACE est destiné à être hérité par des objets utilisateur dans une unité d’organisation, il est probable qu’il ne doit pas être appliqué pour l’accès à l’unité d’organisation elle-même.<br/> |



 

Les **\_ ACEFLAG ADS \_ ne pas se \_ propager \_ hériter \_ ACE** et **ADS \_ ACEFLAG \_ hériter \_ uniquement \_** des indicateurs ACE sont significatifs uniquement si les **publicités \_ ACEFLAG \_ héritent \_** de l’entrée du contrôle d’accès. Cela est dû au fait que l’indicateur **\_ \_ \_ ACE ACEFLAG inherit des publicités** ajoute un comportement d’héritage à une ACE pouvant être héritée, mais ne définit pas le type d’héritage. Les balises **ADS \_ ACEFLAG \_ no \_ propagate \_ inherit \_ ACE** et **ADS \_ ACEFLAG \_ n’héritent \_ que \_** des indicateurs ACE qui définissent un type spécifique de comportement d’héritage.

Il est important de se souvenir que le système définit également les indicateurs suivants en fonction du type et de l’état de l’entrée du contrôle d’accès.



| Indicateur                                    | Description                                           |
|-----------------------------------------|-------------------------------------------------------|
| **\_ \_ ACE hérité ACEFLAG \_ ads**        | Cet indicateur indique que l’entrée du contrôle d’accès a été héritée.       |
| **\_indicateurs d' \_ héritage valides ACEFLAG \_ ADS \_** | Cet indicateur indique que les indicateurs d’héritage sont valides. |



 

Le tableau suivant répertorie les effets des différentes combinaisons d’indicateurs pour la propriété [**AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) d’une entrée du contrôle d’accès.



| Indicateur                                                                                                                    | Effet sur l’objet contenant l’entrée du contrôle d’accès                     | Effet sur les objets enfants directs                                                      | Effet sur les objets en dessous des enfants directs               |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------|
| Aucun indicateur défini.                                                                                                           | ACE effective : l’entrée du contrôle d’accès s’applique à l’objet.               | L’entrée du contrôle d’accès n’est pas héritée.                                                               | L’entrée du contrôle d’accès n’est pas héritée.                                 |
| **\_ACE ACEFLAG \_ hériter des publicités \_**                                                                                          | ACE effectif                                           | L’entrée du contrôle d’accès est héritée. ACE est une entrée du contrôle d’accès effective.<br/>                               | L’entrée du contrôle d’accès est héritée. ACE est une entrée du contrôle d’accès effective.<br/> |
| **Annonces \_ ACEFLAG \_ inherit \_ ACE ACE** \| **\_ ACEFLAG \_ hériter \_ uniquement \_ ACE**                                                  | N’est pas un ACE effectif : l’entrée du contrôle d’accès ne s’applique pas à l’objet. | L’entrée du contrôle d’accès est héritée. ACE est une entrée du contrôle d’accès effective.<br/>                               | L’entrée du contrôle d’accès est héritée. ACE est une entrée du contrôle d’accès effective.<br/> |
| **Annonces \_ ACEFLAG \_ inherit \_ ACE ACE** \| **\_ ACEFLAG \_ no \_ propagate \_ inherit \_ ACE**                                         | ACE effectif                                           | L’entrée du contrôle d’accès est héritée, mais sans indicateurs d’héritage. ACE est un ACE effectif<br/>  | L’entrée du contrôle d’accès n’est pas héritée.                                 |
| **Annonces \_ ACEFLAG \_ hériter \_** des \| **publicités ACE \_ ACEFLAG \_ hériter \_ uniquement \_** des \| **publicités ACE \_ ACEFLAG pas de \_ \_ propagation \_ hériter \_ ACE** | N’est pas une entrée de contrôle d’accès effective.                                   | L’entrée du contrôle d’accès est héritée, mais sans indicateurs d’héritage. ACE est une entrée du contrôle d’accès effective.<br/> | L’entrée du contrôle d’accès n’est pas héritée.                                 |



 

 

