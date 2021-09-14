---
description: Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autostatic, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923300"
---
# <a name="autostatic-element"></a>autostatic, élément

Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques. Ce comportement est activé par défaut.

## <a name="usage"></a>Usage

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



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




