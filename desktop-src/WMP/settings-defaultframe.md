---
title: Paramètres. defaultFrame
description: La propriété defaultFrame spécifie ou récupère le nom du frame utilisé pour afficher une URL reçue dans un événement commande.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Paramètres. defaultFrame Lecteur Windows Media
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
ms.openlocfilehash: 0240864cd19c1a4d84c30abfc6e6b8ecb08457d26c3c660d19fc18d228b19615
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571809"
---
# <a name="settingsdefaultframe"></a>Paramètres. defaultFrame

La propriété **defaultFrame** spécifie ou récupère le nom du frame utilisé pour afficher une URL reçue dans un événement **commande** .

## <a name="syntax"></a>Syntaxe

Player. Settings. defaultFrame

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture qui correspond à la valeur de l’attribut **Name** de l’élément Frame cible.

## <a name="remarks"></a>Remarques

Si un frame cible est spécifié dans l’événement **commande** lui-même, cette propriété est ignorée.

Cette propriété est ignorée lors de l’utilisation de l’applet Java de Netscape Navigator. dans le navigateur, chaque commande de script d’URL reçue affiche l’url dans une nouvelle fenêtre de navigateur, quelle que soit la valeur de *Paramètres*. **defaultFrame**.

**Lecteur Windows Media 10 Mobile**: cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Événement Player. commande**](player-player-scriptcommand.md)
</dt> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> <dt>

[**Utilisation de Windows Media Player avec Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





