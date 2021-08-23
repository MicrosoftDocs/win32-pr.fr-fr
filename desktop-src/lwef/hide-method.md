---
title: Hide, méthode
description: Hide, méthode
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67057464c8e505e56123f712d3a1e6d668c7d75b00bc4732e7b18195b3be9723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725449"
---
# <a name="hide-method"></a>Hide, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Masque le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Masquer_ *  \[ *rapidement*\]



| Partie   | Description                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rapide* | Facultatif. Valeur booléenne qui indique s’il faut ignorer l’animation associée à l’état de masquage du caractère **true** ne joue pas l’animation de **masquage** . <br/> **False** (valeur par défaut) lit l’animation de **masquage** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Le serveur met en file d’attente les actions de la méthode **Hide** dans la file d’attente du caractère. vous pouvez donc l’utiliser pour masquer le caractère après une séquence d’autres animations. Vous pouvez exécuter l’action immédiatement à l’aide de la méthode [**Stop**](stop-method.md) avant d’appeler cette méthode.

Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . En outre, si l’animation de **masquage** associée n’a pas été chargée et que vous n’avez pas spécifié le paramètre **Fast** comme **true**, le serveur définit la propriété [**État**](status-property.md) de l’objet de la **demande** sur « failed » avec un numéro d’erreur approprié. Par conséquent, si vous utilisez le protocole HTTP pour accéder à des données de caractère ou d’animation, utilisez la méthode d' [**extraction**](get-method.md) et spécifiez l’état de **masquage** pour charger l’animation avant d’appeler la méthode **Hide** .

Le masquage d’un caractère peut également entraîner le déclenchement de l’événement [**ActivateInput**](activateinput-event.md) d’un autre client.

> [!Note]  
> Les caractères masqués ne peuvent pas accéder au canal audio. Le serveur renvoie un état d’échec dans l’événement [**RequestComplete**](requestcomplete-event.md) si vous générez une demande d’animation et que le caractère est masqué.

 

## <a name="see-also"></a>Voir aussi

[**Show (méthode)**](show-method.md)


 

