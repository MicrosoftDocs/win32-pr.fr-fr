---
description: Génère des définitions de structure C pour les types de messages.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: élément messageStructureDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a116658fc7ce7f985b7b717c7a7b4ce38be4637
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993666"
---
# <a name="messagestructuredefinitions-element"></a>élément messageStructureDefinitions

Génère des définitions de structure C pour les types de messages.

## <a name="usage"></a>Usage

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
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

Les structures de message sont référencées par le code stub et le proxy générés. Cet élément est utilisé pour générer des fichiers include.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




