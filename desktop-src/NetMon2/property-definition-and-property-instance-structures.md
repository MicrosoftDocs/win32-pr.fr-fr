---
description: Moniteur réseau fournit une structure PROPERTYINFO pour définir les propriétés d’un protocole, et une structure PROPERTYINST et PROPERTYINSTEX pour définir une instance d’une propriété.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Définition de propriété et structures d’instance de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8289c16bf501d36936b1aba6f292787e1b9a41babdb1225d3c0d53885c0ba31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676812"
---
# <a name="property-definition-and-property-instance-structures"></a>Définition de propriété et structures d’instance de propriété

Moniteur réseau fournit une structure [**PROPERTYINFO**](propertyinfo.md) pour définir les propriétés d’un protocole, et une structure [**PROPERTYINST**](propertyinst.md)et [**PROPERTYINSTEX**](propertyinstex.md) pour définir une instance d’une propriété.

![structures du moniteur réseau](images/property1.png)

L’analyseur alloue et remplit la structure [**PROPERTYINFO**](propertyinfo.md) pour toutes les propriétés qu’un protocole prend en charge. L’analyseur passe la structure à Moniteur réseau où la structure est ajoutée à la [*base de données de propriétés de*](p.md)protocole. Les informations contenues dans la structure **PROPERTYINFO** sont utilisées lors de l’analyse d’une instance d’une propriété, ainsi que lors de la mise en forme des données affichées dans l’interface utilisateur Moniteur réseau.

Moniteur réseau alloue les structures [**PROPERTYINST**](propertyinst.md) et [**PROPERTYINSTEX**](propertyinstex.md) lorsque l’analyseur attache une définition de propriété à une instance d’une propriété.

La procédure suivante identifie les étapes nécessaires à l’attachement d’une définition de propriété.

**Pour attacher une définition de propriété**

1.  Identifiez chaque propriété qui existe dans une instance du protocole. Lors de l’attachement d’une définition, Moniteur réseau transmet les données capturées à l’analyseur. Les données sont transmises sur la base d’une instance de protocole.
2.  Déterminez l’emplacement de la propriété dans l’instance de protocole.
3.  Attachez une définition de propriété à l’emplacement de la propriété.

Moniteur réseau implémente une structure [**PROPERTYINST**](propertyinst.md) lorsque l’analyseur utilise les données de propriété telles qu’elles existent dans la capture. Moniteur réseau implémente une structure [**PROPERTYINSTEX**](propertyinstex.md) lorsque l’analyseur doit modifier les données de la propriété dans la capture.

 

 



