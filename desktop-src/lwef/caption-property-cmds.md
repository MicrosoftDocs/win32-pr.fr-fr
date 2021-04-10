---
title: Propriété Caption (objet collection Commands)
description: Propriété Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102688"
---
# <a name="caption-property-commands-collection-object"></a>Propriété Caption (objet collection Commands)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Détermine le texte affiché pour un objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) dans le menu contextuel du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ * [Chaîne Commands. Caption](caption-property.md) \[  =  \]



| Partie     | Description                                                              |
|----------|--------------------------------------------------------------------------|
| *string* | Expression de chaîne qui prend la valeur du texte affiché en tant que légende. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La définition de la propriété [**Caption**](caption-property.md) de votre collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) définit son mode d’affichage dans le menu contextuel du caractère lorsque sa propriété [**visible**](visible-property.md) a la valeur true et que votre application n’est pas le client d’entrée-actif. Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.

Si vous définissez des commandes pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) qui a une [**légende**](caption-property.md), vous définissez généralement une **légende** pour la collection de **commandes** associée.

 

 
