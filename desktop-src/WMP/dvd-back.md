---
title: DVD. Back, méthode
description: La méthode back retourne l’affichage d’un sous-menu à son menu parent.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- Lecteur Windows Media de la méthode back
- méthode back Lecteur Windows Media, DVD, classe
- Lecteur Windows Media de classe DVD, méthode back
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 916c16af578e2ccb6b0e4a6717431f7c30f3084bcd12fbedb1dff9f6c0627493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579088"
---
# <a name="dvdback-method"></a>DVD. Back, méthode

La méthode **Back** retourne l’affichage d’un sous-menu à son menu parent.

## <a name="syntax"></a>Syntaxe


```JScript
DVD.back()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Certains DVD sont créés afin que la méthode **Back** soit disponible dans le menu racine, mais lorsqu’elle est appelée, elle ne fait rien.

**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> </dl>

 

 





