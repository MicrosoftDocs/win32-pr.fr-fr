---
title: Settings. volume
description: La propriété volume spécifie ou récupère le volume actuel.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Settings. volume lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537975"
---
# <a name="settingsvolume"></a>Settings. volume

La propriété **volume** spécifie ou récupère le volume actuel.

## <a name="syntax"></a>Syntaxe

Player. Settings. volume

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**) compris entre 0 et 100.

## <a name="remarks"></a>Notes

Zéro spécifie aucun volume et 100 spécifie le volume complet. Si aucune valeur n’est spécifiée pour cette propriété, le dernier paramètre de volume défini pour le lecteur est utilisé par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 





