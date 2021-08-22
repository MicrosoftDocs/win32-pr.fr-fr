---
description: Est l’élément racine d’un fichier de script XML du générateur de code WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: élément wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ffac9696371f53b073fa71c0b1903c826544a6f695b9b741b48936c0250d2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049537"
---
# <a name="wsdcodegen-element"></a>élément wsdCodeGen

Est l’élément racine d’un fichier de script XML du générateur de code WSDAPI.

## <a name="usage"></a>Usage

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a>Attributs



| Attribut                        | Type                             | Obligatoire       | Description                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| **ConfigFileVersion**<br/> | Toute chaîne de caractères.<br/> | Oui<br/> | Version du fichier de configuration. La seule valeur valide est « 1,0 ».<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Description                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autostatique**](autostatic.md)<br/>                     | Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques. Cette option est activée par défaut.<br/> <br/>                                                                 |
| [**txt**](file.md)<br/>                                 | Indique au générateur de code de générer un fichier.<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | Métadonnées d’hébergement pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | Numéro de la couche de code à générer. Les numéros de couche sont utilisés dans les tables du runtime pour distinguer une couche de code d’une autre. WSDAPI utilise le code généré qui a un numéro de couche 0.<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | Préfixe à utiliser dans le code généré pour garantir l’unicité des symboles générés. WSDAPI utilise le préfixe « WSD ».<br/> <br/>                                                                                     |
| [**macro**](macro.md)<br/>                               | Définit le texte ou CDATA à réutiliser par l’élément [**include**](include.md) .<br/> <br/>                                                                                                                        |
| [**Joint**](namespace.md)<br/>                       | Décrit un espace de noms à utiliser pour la génération de code.<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Décrit l’hôte et les métadonnées hébergées pour l’appareil.<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | Métadonnées du fabricant et du modèle pour l’appareil à implémenter. Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).<br/> <br/>                                                                  |
| [**WSDL**](wsdl.md)<br/>                                 | Spécifie un fichier WSDL à traiter pour les informations de contrat.<br/> <br/>                                                                                                                                           |
| [**XSD**](xsd.md)<br/>                                   | Spécifie un fichier XSD à traiter pour les informations de contrat.<br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a>Éléments parents

Il n’y a pas d’éléments parents.

## <a name="remarks"></a>Remarques

En général, les éléments de [**fichier**](file.md) doivent se produire en dernier, car ils génèrent du code qui utilise des données spécifiées par les autres éléments.

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Valeur |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




