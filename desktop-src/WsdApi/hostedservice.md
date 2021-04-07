---
description: Définit un service à héberger dans une fonction de générateur d’hôte.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: élément service hébergé
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863990"
---
# <a name="hostedservice-element"></a>élément service hébergé

Définit un service à héberger dans une fonction de générateur d’hôte.

## <a name="usage"></a>Utilisation

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
| [**fichier**](file.md)<br/> | Spécification du fichier de sortie pour le générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




