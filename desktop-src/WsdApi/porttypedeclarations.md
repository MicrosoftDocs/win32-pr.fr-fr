---
description: Génère des déclarations de constante C pour les types de port.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: élément portTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e202f1451d93b519bd59ea51f591c37a92957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533826"
---
# <a name="porttypedeclarations-element"></a>élément portTypeDeclarations

Génère des déclarations de constante C pour les types de port.

## <a name="usage"></a>Utilisation

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Baptisé**](codename.md)<br/>   | Spécifie le nom à utiliser pour le type de port dans le code généré. Par défaut, le nom de code est généré à partir du nom qualifié du type de port.<br/> <br/> |
| [**opération**](operation.md)<br/> | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>                                                                                          |
| [**portType**](porttype.md)<br/>   | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**fichier**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Notes

Les déclarations de type de port sont référencées par l’application et une grande partie du code généré. Cet élément est utilisé pour générer des fichiers include.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




