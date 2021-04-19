---
description: Génère des fonctions pour créer des proxies typés.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: élément proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522136"
---
# <a name="proxybuilderimplementations-element"></a>élément proxyBuilderImplementations

Génère des fonctions pour créer des proxies typés.

## <a name="usage"></a>Utilisation

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
| [**fichier**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




