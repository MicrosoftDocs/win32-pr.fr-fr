---
description: Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: élément macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517780"
---
# <a name="macroprefix-element"></a>élément macroPrefix

Définit le préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.

## <a name="usage"></a>Utilisation

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



## <a name="remarks"></a>Notes

Cet élément remplace le préfixe d’URI par défaut utilisé pour les macros générées. Par exemple, si le préfixe de macro est « AV \_ » et que le nom est « tuner », la macro générée pour le nom qualifié sera « \_ tuner AV ».

Par défaut, le code généré crée un préfixe de macro préféré à partir de l’URI.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




