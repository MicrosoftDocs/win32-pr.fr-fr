---
title: Méthode IWMPDVD titleMenu
description: La méthode titleMenu arrête la lecture et affiche le menu du titre.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- Lecteur Windows Media de la méthode titleMenu
- méthode titleMenu Lecteur Windows Media, interface IWMPDVD
- Lecteur Windows Media de l’interface IWMPDVD, méthode titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000459"
---
# <a name="iwmpdvdtitlemenu-method"></a>IWMPDVD :: titleMenu, méthode

La méthode **titleMenu** arrête la lecture et affiche le menu du titre.

## <a name="syntax"></a>Syntaxe


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Chaque DVD est créé différemment. Le DVD doit contenir un menu pour que cette méthode fonctionne. Certains DVD sont créés afin que les méthodes **menu IWMPDVD.** et **titleMenu** ouvrent le même menu. La méthode **titleMenu** appelle généralement le menu du titre, mais elle peut appeler le menu supérieur si aucun menu de titre n’est disponible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**menu IWMPDVD. (VB et C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





