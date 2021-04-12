---
description: Définit le numéro de la couche de code à générer.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: élément layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203149"
---
# <a name="layernumber-element"></a>élément layerNumber

Définit le numéro de la couche de code à générer.

## <a name="usage"></a>Utilisation

``` syntax
<layerNumber/>
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

Les numéros de couche sont utilisés dans les tables du runtime pour distinguer une couche de code d’une autre. WSDAPI utilise le code généré qui a un numéro de couche 0.

En général, cette valeur est 1, ce qui indique que le code généré est superposé au-dessus de WSDAPI et aucune autre couche. Dans certains cas, des nombres plus élevés peuvent être utilisés. Par exemple, si une société produit du code pour une classe d’appareil (couche 1 numérotée), un fournisseur de matériel particulier peut souhaiter ajouter une couche 2 supplémentaire numérotée à la couche.

Les valeurs autorisées, sauf dans le cas de WSDAPI lui-même sont supérieures à 0 et inférieures à 16.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




