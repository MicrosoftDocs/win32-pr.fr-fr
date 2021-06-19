---
title: Visible, propriété (objet Characters)
description: En savoir plus sur la propriété visible de l’objet Characters, qui retourne une valeur booléenne indiquant si le caractère est visible.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396304"
---
# <a name="visible-property-characters-object"></a>Visible, propriété (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur booléenne indiquant si le caractère est visible.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent ***. Caractères (**"* CharacterID *" * *). Visible**



| Valeur | Description                            |
|-------|----------------------------------------|
| True  | Le caractère est affiché.            |
| False | Le caractère est masqué (non visible). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette propriété indique si le frame du caractère est affiché. Cela ne signifie pas nécessairement qu’il y a une image à l’écran. Par exemple, cette propriété retourne la **valeur true** même si le caractère est positionné en dehors de la zone d’affichage visible ou lorsque le frame de caractères actuel ne contient aucune image. Le paramètre de cette propriété s’applique à tous les clients du caractère.

Cette propriété est en lecture seule. Pour rendre un caractère visible ou masqué, utilisez les méthodes d' [**affichage**](show-method.md) ou de [**masquage**](https://www.bing.com/search?q=**Hide**) .

 

 




