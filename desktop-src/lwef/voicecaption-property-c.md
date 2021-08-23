---
title: Propriété VoiceCaption (objet Command)
description: En savoir plus sur la propriété VoiceCaption de l’objet Command, qui définit ou retourne le texte affiché pour l’objet Command dans la fenêtre commandes vocales.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1e911a4351483aeeea9258679d4321110b49c3d0c51fc49282701b027d27e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665049"
---
# <a name="voicecaption-property-command-object"></a>Propriété VoiceCaption (objet Command)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Définit ou retourne le texte affiché pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) dans la fenêtre commandes vocales.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Commandes («_*_nom_*_»)._ *  \[  =  *Chaîne* VoiceCaption\]



| Partie     | Description                                               |
|----------|-----------------------------------------------------------|
| *string* | Expression de chaîne qui prend la valeur du texte affiché. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Si vous définissez un objet de [**commande**](/windows/desktop/lwef/the-command-object) dans une collection de [**commandes**](https://www.bing.com/search?q=**Commands**) et que vous définissez sa propriété [**Voice**](voice-property.md) , vous définissez en général également sa propriété [**VoiceCaption**](voicecaption-property.md) . Ce texte s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible. Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) détermine le texte affiché. Lorsque ni la propriété **VoiceCaption** ni la propriété **Caption** n’est définie, la commande n’apparaît pas dans la fenêtre commandes vocales.

### <a name="see-also"></a>Voir aussi

[**Propriété Caption**](caption-property.md)


 

 
