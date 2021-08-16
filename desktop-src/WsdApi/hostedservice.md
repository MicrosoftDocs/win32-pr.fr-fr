---
description: Définit un service à héberger dans une fonction de générateur d’hôte.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: élément service hébergé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08479e88214e5fe6d1fbbb6ff5a3fffb7bb2047e8b7ca08cde92d64dd7dd6b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130791"
---
# <a name="hostedservice-element"></a>élément service hébergé

Définit un service à héberger dans une fonction de générateur d’hôte.

## <a name="usage"></a>Usage

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                     | Description                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Baptisé**](codename.md)<br/>     | Spécifie le nom à utiliser pour le type de port dans le code généré. Par défaut, le nom de code est généré à partir du nom qualifié du type de port.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Type de port pour lequel le code doit être généré.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Nom de la classe à générer à partir de la fonction de générateur.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | URI qui représente l’identificateur de service.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**txt**](file.md)<br/> | Spécification du fichier de sortie pour le générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




