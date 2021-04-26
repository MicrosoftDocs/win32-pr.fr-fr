---
description: Définit le préfixe à utiliser dans le code généré pour garantir l’unicité des symboles générés.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: élément layerPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98970013c72600affd7d4d9e7a71781f477cd87d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994696"
---
# <a name="layerprefix-element"></a>élément layerPrefix

Définit le préfixe à utiliser dans le code généré pour garantir l’unicité des symboles générés.

## <a name="usage"></a>Usage

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Remarques

Chaque script de générateur de code doit définir une chaîne de préfixe unique pour les modules créés. Par exemple, les scripts de cadre d’image utilisent le préfixe « PFDEMO ».

WSDAPI utilise le préfixe « WSD ».

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




