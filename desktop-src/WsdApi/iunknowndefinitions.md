---
description: Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Élément IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524991"
---
# <a name="iunknowndefinitions-element"></a>Élément IUnknownDefinitions

Génère des implémentations pour les fonctions QueryInterface, AddRef et Release.

## <a name="usage"></a>Utilisation

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
| [**fichier**](file.md)<br/> | Génère un fichier à partir du générateur de code.<br/> <br/> |



## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Non            |



 

 




