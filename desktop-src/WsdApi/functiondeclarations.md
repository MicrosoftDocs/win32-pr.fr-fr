---
description: Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: élément functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 449bc6706a83c0c7eec9af7a4b8d05c60089705dce38e4ed1d87a2b2dc1d542d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954849"
---
# <a name="functiondeclarations-element"></a>élément functionDeclarations

Génère des déclarations d’implémentation pour les fonctions de proxy pour les opérations de type de port.

## <a name="usage"></a>Usage

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Suppr**](async.md)<br/>         | Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.<br/> <br/>         |
| [**événements**](events.md)<br/>       | Spécifie si les événements connexes sont inclus dans les fonctions générées.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.<br/> <br/> |
| [**operation**](operation.md)<br/> | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet élément génère des déclarations de fonctions membres correspondant aux opérations appelées par le contrat. Ces déclarations sont dans un format approprié à la consommation par un compilateur C++ et sont généralement utilisées dans les fichiers. cpp.

Exemple :

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




