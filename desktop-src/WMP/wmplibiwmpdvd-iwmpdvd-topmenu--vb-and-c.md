---
title: IWMPDVD, méthode de menu
description: La méthode de menu principal arrête la lecture et affiche le menu supérieur (ou racine) du titre actuel.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Lecteur Windows Media de la méthode de menu
- méthode de menu Lecteur Windows Media, interface IWMPDVD
- Lecteur Windows Media de l’interface IWMPDVD, méthode de menu
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403700"
---
# <a name="iwmpdvdtopmenu-method"></a>IWMPDVD :: keymenu, méthode

La méthode de **menu** principal arrête la lecture et affiche le menu supérieur (ou racine) du titre actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Le DVD doit contenir un menu pour que cette méthode fonctionne. Certains DVD sont créés afin que les méthodes **menu** et **IWMPDVD. titleMenu** ouvrent le même menu. La méthode de **menu** principal appelle généralement le menu supérieur (ou racine), mais elle peut appeler le menu de titre si aucun menu racine n’est disponible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB et C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





