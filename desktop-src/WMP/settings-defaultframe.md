---
title: Paramètres. defaultFrame
description: La propriété defaultFrame spécifie ou récupère le nom du frame utilisé pour afficher une URL reçue dans un événement commande.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528515"
---
# <a name="settingsdefaultframe"></a>Paramètres. defaultFrame

La propriété **defaultFrame** spécifie ou récupère le nom du frame utilisé pour afficher une URL reçue dans un événement **commande** .

## <a name="syntax"></a>Syntaxe

Player. Settings. defaultFrame

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture qui correspond à la valeur de l’attribut **Name** de l’élément Frame cible.

## <a name="remarks"></a>Notes

Si un frame cible est spécifié dans l’événement **commande** lui-même, cette propriété est ignorée.

Cette propriété est ignorée lors de l’utilisation de l’applet Java de Netscape Navigator. Dans le navigateur, chaque commande de script d’URL reçue affiche l’URL dans une nouvelle fenêtre de navigateur, quelle que soit la valeur des *paramètres*. **defaultFrame**.

**Windows Media Player 10 Mobile**: cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Événement Player. commande**](player-player-scriptcommand.md)
</dt> <dt>

[**Settings (objet)**](settings-object.md)
</dt> <dt>

[**Utilisation de Windows Media Player avec Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





