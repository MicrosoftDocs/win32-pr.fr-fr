---
title: Méthode DVD. titleMenu
description: La méthode titleMenu arrête la lecture du titre et affiche le menu du titre.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- méthode titleMenu lecteur Windows Media
- méthode titleMenu lecteur Windows Media, DVD, classe
- Classe DVD lecteur Windows Media, méthode titleMenu
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
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317213"
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

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Le DVD doit contenir un menu pour que cette méthode fonctionne. Certains DVD sont créés afin que les méthodes **menu** et **titleMenu** ouvrent le même menu. La méthode **titleMenu** appelle généralement le menu de titre, mais elle peut appeler le menu supérieur à la place, si aucun menu de titre n’est disponible.

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

[**Menu DVD.**](dvd-topmenu.md)
</dt> </dl>

 

 





