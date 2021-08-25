---
description: Génère une déclaration pour une fonction qui crée un hôte typé.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: élément hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172181313f4cc95500fe61a922b119bba1fc02515d0e912289eb6d9ac8f8fc86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794219"
---
# <a name="hostbuilderdeclaration-element"></a>élément hostBuilderDeclaration

Génère une déclaration pour une fonction qui crée un hôte typé.

## <a name="usage"></a>Usage

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**interface**](interface.md)<br/> | Nom de l’interface de service à inclure pour l’hôte. La valeur de cet élément doit correspondre à la valeur de l’élément enfant de l' [**interface**](interface.md) de [**service hébergé**](hostedservice.md). <br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
interface+
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**txt**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




