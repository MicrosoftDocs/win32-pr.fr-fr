---
title: Application, élément
description: représente l’élément de niveau supérieur dans la spécification du balisage de l’infrastructure du ruban Windows.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- ruban Windows élément d’Application
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4055e271ecf3313596b73aa36a5cbea37250416d9b517fb4512b89fbc203293a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810809"
---
# <a name="application-element"></a>Application, élément

représente l’élément de niveau supérieur dans la spécification du balisage de l’infrastructure du ruban Windows.

## <a name="usage"></a>Usage

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Attributs



| Attribut            | Type                 | Obligatoire       | Description                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Oui<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> URI de la liaison d’espace de noms du balisage du ruban. <br/> </dd> </dl> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                               | Description                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application. commandes**](windowsribbon-element-application-commands.md)<br/> | Peut se produire au plus une fois<br/> <br/>  |
| [**Application. views**](windowsribbon-element-application-views.md)<br/>       | Doit se produire exactement une fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents

Il n’y a pas d’éléments parents.

## <a name="remarks"></a>Remarques

Obligatoire.

Doit se produire exactement une fois comme conteneur pour l’ensemble du balisage du ruban.

Les éléments enfants de l’élément **application** doivent se produire dans l’ordre spécifié :

1.  [**Application. commandes**](windowsribbon-element-application-commands.md)
2.  [**Application. views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Exemples

L’exemple suivant illustre une déclaration d’élément d' **application** .


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Informations sur les éléments



|                                     |           |
|-------------------------------------|-----------|
| Système minimal pris en charge<br/> | Windows 7 |
| Peut être vide                        | Non        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](windowsribbon-schema.md)
</dt> </dl>

 

 





