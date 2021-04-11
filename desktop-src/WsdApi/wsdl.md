---
description: Spécifie un fichier WSDL à traiter pour les informations de contrat.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: élément wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202989"
---
# <a name="wsdl-element"></a>élément wsdl

Spécifie un fichier WSDL à traiter pour les informations de contrat.

## <a name="usage"></a>Utilisation

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                           | Description                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un <élément wsdl : import> dans un fichier WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Spécifie l’emplacement de téléchargement pour un <directive wsdl : import> qui ne spécifie pas explicitement d’emplacement.<br/> <br/>           |
| [**d**](path.md)<br/>                   | Fichier et chemin d’accès du fichier d’entrée WSDL.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Notes

Tout élément [**importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) apparaissant après l’élément [**path**](path.md) dans un fichier de configuration XML sera ignoré.

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




