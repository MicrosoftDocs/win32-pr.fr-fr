---
description: Tous les objets Item ont des propriétés.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Attributs de propriété (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdee1cdee48bba6183f9bcae2abc521ac9f53dfb33eec544ab3ed6bead4947b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007529"
---
# <a name="property-attributes-wia"></a>Attributs de propriété (WIA)

Tous les objets Item ont des propriétés. Les propriétés ont des attributs. Par exemple, les attributs de propriété indiquent si une propriété est lue, écrite ou supprimée. Ils indiquent également les valeurs de propriété valides. Les constantes suivantes sont des attributs de propriété valides : 

| Attribut de propriété        | Signification                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| WIA \_ prop \_ cacheable      | L’appareil peut mettre en cache la valeur de la propriété.                                                               |
| \_indicateur de prop WIA \_           | La propriété a une liste de valeurs d’indicateur autorisées. Les valeurs d’indicateur sont combinées à l’aide d' **une opération or** au niveau du bit. |
| \_liste de propriétés WIA \_           | La propriété a une liste de valeurs autorisées.                                                                 |
| WIA \_ prop \_ None           | Aucune valeur valide n’est associée à la propriété.                                          |
| \_plage de prop WIA \_          | La propriété a une plage de valeurs valides.                                                                |
| \_lecture WIA prop \_           | L’application peut lire la valeur de la propriété.                                                           |
| WIA \_ prop \_ RW             | L’application peut lire et écrire la valeur de la propriété.                                                 |
| \_synchronisation WIA \_ prop \_ requise | Ne pas utiliser.                                                                                              |
| \_écriture WIA prop \_          | L’application peut écrire la valeur de la propriété.                                                          |



 

 

 



