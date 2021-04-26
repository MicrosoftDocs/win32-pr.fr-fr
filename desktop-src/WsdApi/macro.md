---
description: Définit le texte ou CDATA à réutiliser par l’élément Include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994326"
---
# <a name="macro-element"></a>macro, élément

Définit le texte ou CDATA à réutiliser par l’élément [**include**](include.md) .

## <a name="usage"></a>Usage

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



## <a name="remarks"></a>Remarques

WsdCodeGen définit une macro nommée **DoNotModify**. Lorsque cette macro est incluse, le code généré contient un bloc de commentaires de visibilité élevée qui indique aux développeurs qu’ils ne peuvent pas modifier le code généré.

Le code XML suivant montre comment inclure la macro **DoNotModify** . Ce code XML peut être ajouté à un fichier de configuration XML pour WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




