---
title: Visible, propriété (objet Characters)
description: Propriété visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510292"
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
| Faux | Le caractère est masqué (non visible). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété indique si le frame du caractère est affiché. Cela ne signifie pas nécessairement qu’il y a une image à l’écran. Par exemple, cette propriété retourne la **valeur true** même si le caractère est positionné en dehors de la zone d’affichage visible ou lorsque le frame de caractères actuel ne contient aucune image. Le paramètre de cette propriété s’applique à tous les clients du caractère.

Cette propriété est en lecture seule. Pour rendre un caractère visible ou masqué, utilisez les méthodes d' [**affichage**](show-method.md) ou de [**masquage**](https://www.bing.com/search?q=**Hide**) .

 

 




