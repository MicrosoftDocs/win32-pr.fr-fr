---
description: Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.
ms.assetid: 17556708-9350-444f-84a3-d982270b31d1
title: élément messageTypeDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696cd6d30e6a791f68c152e0d0c5d0b1a7300769
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998726"
---
# <a name="messagetypedeclarations-element"></a>élément messageTypeDeclarations

Génère des déclarations de constante C pour les tables de schéma XML pour les types de messages.

## <a name="usage"></a>Usage

``` syntax
<messageTypeDeclarations>
  child elements
</messageTypeDeclarations>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**opération**](operation.md)<br/> | Spécifie une opération pour laquelle du code doit être généré.<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | Spécifie le type de port pour lequel le code doit être généré.<br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="remarks"></a>Remarques

Les tables de schéma sont référencées par des définitions de type de port. Cet élément est donc généralement utilisé juste avant les éléments [**portTypeDefinitions**](porttypedefinitions.md) .

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




