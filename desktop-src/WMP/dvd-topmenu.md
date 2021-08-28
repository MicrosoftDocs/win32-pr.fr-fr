---
title: DVD. up, méthode de menu
description: La méthode de menu principal arrête la lecture du titre et affiche le menu supérieur (ou racine) du titre actuel.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Lecteur Windows Media de la méthode de menu
- méthode de menu Lecteur Windows Media, DVD, classe
- Lecteur Windows Media de classe DVD, méthode de menu
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
ms.openlocfilehash: e6042547d26d40c620da503836de1ec15991280b17dd066cf81d32c617e85064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651159"
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

## <a name="remarks"></a>Remarques

Chaque DVD est créé différemment. Le DVD doit contenir un menu pour que cette méthode fonctionne. Certains DVD sont créés afin que les méthodes **menu** et **titleMenu** ouvrent le même menu. La méthode de **menu** principal appelle généralement le menu supérieur (ou racine), mais elle peut appeler le menu titre à la place, si aucun menu racine n’est disponible.

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
</dt> <dt>

[**DVD. titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





