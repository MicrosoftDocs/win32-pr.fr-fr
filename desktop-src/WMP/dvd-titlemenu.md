---
title: Méthode DVD. titleMenu
description: La méthode titleMenu arrête la lecture du titre et affiche le menu du titre.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- Lecteur Windows Media de la méthode titleMenu
- méthode titleMenu Lecteur Windows Media, DVD, classe
- Lecteur Windows Media de classe DVD, méthode titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1954ea52d5a67dc502278c7f1e821a06c4e2b849dc4040e690275b6d1b0ef0bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996879"
---
# <a name="dvdtitlemenu-method"></a>Méthode DVD. titleMenu

La méthode **titleMenu** arrête la lecture du titre et affiche le menu du titre.

## <a name="syntax"></a>Syntaxe


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Chaque DVD est créé différemment. Le DVD doit contenir un menu pour que cette méthode fonctionne. Certains DVD sont créés afin que les méthodes **menu** et **titleMenu** ouvrent le même menu. La méthode **titleMenu** appelle généralement le menu de titre, mais elle peut appeler le menu supérieur à la place, si aucun menu de titre n’est disponible.

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

[**Menu DVD.**](dvd-topmenu.md)
</dt> </dl>

 

 





