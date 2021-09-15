---
description: Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Élément IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413281"
---
# <a name="iunknowndefinitions-element"></a>Élément IUnknownDefinitions

Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.

## <a name="usage"></a>Usage

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>Attributs



| Attribut                  | Type                         | Obligatoire       | Description                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | chaîne de caractères \_<br/> | Oui<br/> | Nom de la classe d’implémentation.<br/> <br/> |
| **refCountVar**<br/> | chaîne de caractères \_<br/> | Oui<br/> | Nom de la variable du décompte de références.<br/> <br/>  |



## <a name="child-elements"></a>Éléments enfants



| Élément                                   | Description                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**interface**](interface.md)<br/> | Nom de l’interface à retourner par QueryInterface.<br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
interface
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



 

 




