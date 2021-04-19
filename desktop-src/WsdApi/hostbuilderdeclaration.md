---
description: Génère une déclaration pour une fonction qui crée un hôte typé.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: élément hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522173"
---
# <a name="hostbuilderdeclaration-element"></a>élément hostBuilderDeclaration

Génère une déclaration pour une fonction qui crée un hôte typé.

## <a name="usage"></a>Utilisation

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
| [**fichier**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




