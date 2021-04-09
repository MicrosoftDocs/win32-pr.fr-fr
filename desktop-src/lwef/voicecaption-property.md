---
title: Propriété VoiceCaption (objet Commands)
description: Propriété VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739477"
---
# <a name="voicecaption-property-commands-object"></a>Propriété VoiceCaption (objet Commands)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le texte affiché pour l’objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) dans la fenêtre commandes vocales.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). Chaîne Commands. VoiceCaption_ *  \[  =  \]



| Partie     | Description                                               |
|----------|-----------------------------------------------------------|
| *string* | Expression de chaîne qui prend la valeur du texte affiché. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous définissez la propriété [**Voice**](voice-property.md) de votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) , vous définissez en général également sa propriété **VoiceCaption** . Le paramètre de texte **VoiceCaption** s’affiche dans la fenêtre commandes vocales lorsque votre application cliente est en entrée-active et que le caractère est visible. Si cette propriété n’est pas définie, le paramètre de la propriété [**Caption**](caption-property.md) de la collection **Commands** détermine le texte affiché. Lorsque ni la propriété **VoiceCaption** ni **Caption** n’est définie, les commandes de la collection s’affichent dans la fenêtre commandes vocales sous « (commande non définie) » lorsque votre application cliente devient entrée-active.

Le paramètre **VoiceCaption** détermine également le texte affiché dans l’info-bulle d’écoute pour indiquer les commandes que le caractère écoute.

## <a name="see-also"></a>Voir aussi

[Propriété Caption](caption-property.md)


 

 
