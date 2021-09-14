---
description: Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: élément idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918616"
---
# <a name="idlfunctiondeclarations-element"></a>élément idlFunctionDeclarations

Génère des déclarations IDL pour les fonctions de proxy pour les opérations de type de port.

## <a name="usage"></a>Usage

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Suppr**](async.md)<br/>         | Spécifie si les opérations asynchrones sont incluses dans les fonctions proxy générées.<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | Spécifie si les arguments d’événement associés sont inclus dans les fonctions générées.<br/> <br/>               |
| [**événements**](events.md)<br/>       | Spécifie si les événements connexes sont inclus dans les fonctions générées.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | Spécifie si les paramètres utilisés pour passer les informations d’erreur sont inclus dans les fonctions générées.<br/> <br/> |
| [**opération**](operation.md)<br/> | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                                       |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet élément génère des déclarations de fonctions membres correspondant aux opérations appelées par le contrat. Ces déclarations sont dans un format approprié à la consommation par le compilateur MIDL et sont généralement utilisées dans les fichiers. idl.

Exemple :

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




