---
description: Spécifie un fichier WSDL à traiter pour les informations de contrat.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: élément wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef4bc7b76ce22184e4c2f1ceaa2131ef163a26d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994706"
---
# <a name="wsdl-element"></a>élément wsdl

Spécifie un fichier WSDL à traiter pour les informations de contrat.

## <a name="usage"></a>Usage

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
| [**excludeImport**](excludeimport.md)<br/> | Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un \<wsdl:import> élément d’un fichier WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Spécifie l’emplacement de téléchargement pour une \<wsdl:import> directive qui ne spécifie pas explicitement d’emplacement.<br/> <br/>           |
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



## <a name="remarks"></a>Remarques

Tout élément [**importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) apparaissant après l’élément [**path**](path.md) dans un fichier de configuration XML sera ignoré.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




