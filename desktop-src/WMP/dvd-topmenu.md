---
title: DVD. up, méthode de menu
description: La méthode de menu principal arrête la lecture du titre et affiche le menu supérieur (ou racine) du titre actuel.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- méthode du menu vers le lecteur Windows Media
- méthode menu du lecteur Windows Media, DVD, classe
- Classe DVD lecteur Windows Media, méthode de menu
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465750"
---
# <a name="dvdtopmenu-method"></a>DVD. up, méthode de menu

La méthode de **menu** principal arrête la lecture du titre et affiche le menu supérieur (ou racine) du titre actuel.

## <a name="syntax"></a>Syntaxe


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Le DVD doit contenir un menu pour que cette méthode fonctionne. Certains DVD sont créés afin que les méthodes **menu** et **titleMenu** ouvrent le même menu. La méthode de **menu** principal appelle généralement le menu supérieur (ou racine), mais elle peut appeler le menu titre à la place, si aucun menu racine n’est disponible.

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
</dt> <dt>

[**DVD. titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





