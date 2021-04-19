---
description: Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autostatic, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524147"
---
# <a name="autostatic-element"></a>autostatic, élément

Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques. Ce comportement est activé par défaut.

## <a name="usage"></a>Utilisation

``` syntax
<autoStatic/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Notes

L’élément **autostatique** n’est pas obligatoire et peut être omis dans le fichier de configuration XML. L’élément peut être utilisé pour désactiver le marquage des champs générés comme statiques ou pour forcer explicitement le marquage de certains champs générés comme statiques.

Les valeurs possibles sont 1 (activé, valeur par défaut) et 0 (désactivé). L’activation d' **autostatique** peut entraîner des problèmes de compilation en fonction de la façon dont le générateur de code est dirigé vers les données de sortie.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




