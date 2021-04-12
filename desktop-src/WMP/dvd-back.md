---
title: DVD. Back, méthode
description: La méthode back retourne l’affichage d’un sous-menu à son menu parent.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- méthode back du lecteur Windows Media
- méthode back lecteur Windows Media, DVD, classe
- Classe DVD lecteur Windows Media, méthode back
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
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384667"
---
# <a name="dvdback-method"></a>DVD. Back, méthode

La méthode **Back** retourne l’affichage d’un sous-menu à son menu parent.

## <a name="syntax"></a>Syntaxe


```JScript
DVD.back()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Certains DVD sont créés afin que la méthode **Back** soit disponible dans le menu racine, mais lorsqu’elle est appelée, elle ne fait rien.

**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> </dl>

 

 





