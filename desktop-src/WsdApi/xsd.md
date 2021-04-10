---
description: Spécifie un fichier XSD à traiter pour les informations de contrat.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: élément xsd
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865337"
---
# <a name="xsd-element"></a>élément xsd

Spécifie un fichier XSD à traiter pour les informations de contrat.

## <a name="usage"></a>Utilisation

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



## <a name="remarks"></a>Notes

La chaîne de nom de fichier doit également inclure des informations de chemin d’accès complètes.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




