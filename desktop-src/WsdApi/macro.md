---
description: Définit le texte ou CDATA à réutiliser par l’élément Include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203148"
---
# <a name="macro-element"></a>macro, élément

Définit le texte ou CDATA à réutiliser par l’élément [**include**](include.md) .

## <a name="usage"></a>Utilisation

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Attributs



| Attribut           | Type                         | Obligatoire       | Description                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | chaîne de caractères \_<br/> | Oui<br/> | Nom de la macro.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Notes

WsdCodeGen définit une macro nommée **DoNotModify**. Lorsque cette macro est incluse, le code généré contient un bloc de commentaires de visibilité élevée qui indique aux développeurs qu’ils ne peuvent pas modifier le code généré.

Le code XML suivant montre comment inclure la macro **DoNotModify** . Ce code XML peut être ajouté à un fichier de configuration XML pour WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




