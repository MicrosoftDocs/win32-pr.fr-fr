---
title: Propriété Caption (objet Command)
description: Propriété Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106538603"
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

 

 
