---
title: StopAll, méthode
description: StopAll, méthode
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510253"
---
# <a name="stopall-method"></a>StopAll, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Arrête toutes les demandes d’animation ou les types de demandes spécifiés pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). StopAll*, *  \[ *type*\]



| Partie   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type* | Optionnel. Pour utiliser ce paramètre, vous pouvez utiliser l’une des valeurs suivantes. Vous pouvez également spécifier plusieurs types en les séparant par des virgules. <br/> «**Récupérer**» <br/> Pour arrêter toutes les demandes d' [**extraction**](get-method.md) mises en file d’attente.<br/> «**NonQueuedGet**» <br/> Pour arrêter toutes les demandes d' [**extraction**](get-method.md) non mises en file d’attente (la méthode d'**extraction** avec le paramètre de **file d’attente** a la valeur **false**).<br/> «**Déplacer**» <br/> Pour arrêter toutes les demandes [**MoveTo**](moveto-method.md) mises en file d’attente.<br/> «**Lecture**» <br/> Pour arrêter toutes les demandes de [**lecture**](play-method.md) mises en file d’attente.<br/> «**Speak**» <br/> Pour arrêter toutes les demandes [**Speak**](speak-method.md) mises en file d’attente.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous ne définissez pas le paramètre de **type** , le serveur arrête toutes les animations pour le caractère, y compris les demandes d' [**extraction**](get-method.md) mises en file d’attente et non mises en file d’attente, et efface sa file d’attente d’animation. Elle arrête également la diffusion d’un caractère masqué ou présentant une animation.

Cette méthode ne génère pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Voir aussi

[**Stop, méthode**](stop-method.md)


 

