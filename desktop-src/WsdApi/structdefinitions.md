---
description: Génère des définitions de structure C pour les types connus.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: élément structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c8ad894a42bbafd183031849e458ad5f3bf155a9ccba4e704321e875163c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611559"
---
# <a name="structdefinitions-element"></a>élément structDefinitions

Génère des définitions de structure C pour les types connus.

## <a name="usage"></a>Usage

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Remarques

Les structures des types connus sont référencées par une grande partie du code généré et par le code de l’application. Cet élément est utilisé pour générer des fichiers include. Cet élément doit se produire après un élément [**structDeclarations**](structdeclarations.md) afin que les références entre les structures soient gérées correctement.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




