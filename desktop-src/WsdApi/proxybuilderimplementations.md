---
description: Génère des fonctions pour créer des proxies typés.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: élément proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996466"
---
# <a name="proxybuilderimplementations-element"></a>élément proxyBuilderImplementations

Génère des fonctions pour créer des proxies typés.

## <a name="usage"></a>Usage

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                     | Description                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Baptisé**](codename.md)<br/>     | Nom à utiliser pour le type de port dans le code généré. Par défaut, le nom de code est généré à partir du nom qualifié du type de port.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Type de port pour lequel le code doit être généré.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Nom de classe à générer à partir de la fonction de générateur de proxy.<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




