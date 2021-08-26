---
description: Spécifie un fichier XSD à traiter pour les informations de contrat.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: élément xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f790375c34a4d5afc3dc345691c8e26e5f95cebe0bbde283e2986e838cce554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995089"
---
# <a name="xsd-element"></a>élément xsd

Spécifie un fichier XSD à traiter pour les informations de contrat.

## <a name="usage"></a>Usage

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>Attributs



| Attribut           | Type                       | Obligatoire       | Description                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | chaîne du chemin d’accès<br/> | Oui<br/> | Fichier et chemin d’accès du fichier d’entrée XSD.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                               | Description                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | Spécifie un type à inclure à partir d’un fichier XSD.<br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
typeUri*
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Remarques

La chaîne de nom de fichier doit également inclure des informations de chemin d’accès complètes.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




