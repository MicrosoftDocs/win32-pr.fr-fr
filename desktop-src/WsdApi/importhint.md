---
description: 'Spécifie l’emplacement de téléchargement pour une directive wsdl : import qui ne spécifie pas explicitement d’emplacement.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: élément importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29fcd65f9af02b8077ba828081ac9ed767d64e3
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380653"
---
# <a name="importhint-element"></a>élément importHint

Spécifie l’emplacement de téléchargement pour une \<wsdl:import> directive qui ne spécifie pas explicitement d’emplacement.

## <a name="usage"></a>Usage

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**location**](location.md)<br/>   | Emplacement du fichier à importer. L’emplacement peut être un chemin d’accès relatif, un chemin d’accès absolu ou une URL HTTP.<br/> <br/> |
| [**Joint**](namespace.md)<br/> | Espace de noms à importer. Cela doit correspondre à l’espace de noms spécifié dans l' \<wsdl:import> élément.<br/> <br/>     |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Spécifie un fichier WSDL à traiter pour les informations de contrat.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




