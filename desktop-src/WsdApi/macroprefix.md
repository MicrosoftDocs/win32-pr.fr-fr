---
description: Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: élément macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 970232b86aa226f16fa06cf2d3c9de40c156702c802c6f6254e45157e1df58ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130711"
---
# <a name="macroprefix-element"></a>élément macroPrefix

Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.

## <a name="usage"></a>Usage

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                   | Description                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**Joint**](namespace.md)<br/> | Espace de noms à utiliser pour la génération de code.<br/> <br/> |



## <a name="remarks"></a>Remarques

Cet élément remplace le préfixe d’URI par défaut utilisé pour les macros générées. Par exemple, si le préfixe de macro est « AV \_ » et que le nom est « tuner », la macro générée pour le nom qualifié sera « \_ tuner AV ».

Par défaut, le code généré crée un préfixe de macro préféré à partir de l’URI.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




