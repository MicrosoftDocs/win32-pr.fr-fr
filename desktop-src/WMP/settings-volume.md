---
title: Paramètres. volume
description: La propriété volume spécifie ou récupère le volume actuel.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Lecteur Windows Media Paramètres. volume
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
ms.openlocfilehash: 1c02952426a78323421fd779b253136c1777d509141d51b590b9db40c4d077a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002209"
---
# <a name="settingsvolume"></a>Paramètres. volume

La propriété **volume** spécifie ou récupère le volume actuel.

## <a name="syntax"></a>Syntaxe

Player. Settings. volume

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**) compris entre 0 et 100.

## <a name="remarks"></a>Remarques

Zéro spécifie aucun volume et 100 spécifie le volume complet. Si aucune valeur n’est spécifiée pour cette propriété, le dernier paramètre de volume défini pour le lecteur est utilisé par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





