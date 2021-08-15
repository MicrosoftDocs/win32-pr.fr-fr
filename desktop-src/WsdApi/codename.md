---
description: Définit le nom à utiliser pour identifier l’espace de noms dans le code généré.
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: élément codeName
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e778e6d55e9902ec03597d7776afce9850a93be18f578416246908310fa666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991769"
---
# <a name="codename-element"></a>élément codeName

Définit le nom à utiliser pour identifier l’espace de noms dans le code généré.

## <a name="usage"></a>Usage

``` syntax
<codeName/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                         | Description                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**Joint**](namespace.md)<br/>                       | Espace de noms à utiliser pour la génération de code.<br/> <br/>       |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/> | Génère des déclarations de constante C pour les types de port.<br/> <br/> |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>   | Génère des constantes C pour les types de ports.<br/> <br/>             |



## <a name="remarks"></a>Remarques

Cet élément substitue le nom de code par défaut utilisé pour le code généré. Par défaut, le code généré crée un nom de code à partir de l’URI ou du nom qualifié.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




