---
description: Définit le nom à utiliser pour identifier l’espace de noms dans le code généré.
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: élément codeName
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be7292135e79477d0a66d2a0667ebd51bd7567c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292778"
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



## <a name="remarks"></a>Notes

Cet élément substitue le nom de code par défaut utilisé pour le code généré. Par défaut, le code généré crée un nom de code à partir de l’URI ou du nom qualifié.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




