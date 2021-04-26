---
description: Génère des définitions de structure C pour les types connus.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: élément structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996456"
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



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




