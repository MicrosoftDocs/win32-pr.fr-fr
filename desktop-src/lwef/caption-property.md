---
title: Propriété Caption (objet Command)
description: En savoir plus sur la propriété Caption de l’objet Command. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518445"
---
# <a name="caption-property-command-object"></a>Propriété Caption (objet Command)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Détermine le texte affiché pour une [**commande**](/windows/desktop/lwef/the-command-object) dans le menu contextuel du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_*_»)._ *  \[  =  *Chaîne* de légende\]



| Partie     | Description                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Expression de chaîne qui prend la valeur du texte affiché en tant que légende de la **commande**. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Pour spécifier une touche d’accès (mnémonique non linéaire) pour votre **légende**, incluez un caractère perluète (&) avant ce caractère.

Si vous ne définissez pas de **VoiceCaption** pour votre commande, votre paramètre de **légende** est utilisé.

 

 
