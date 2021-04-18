---
title: Méthode IWMPDVD titleMenu
description: La méthode titleMenu arrête la lecture et affiche le menu du titre.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- méthode titleMenu lecteur Windows Media
- méthode titleMenu lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, méthode titleMenu
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
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526440"
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

## <a name="remarks"></a>Notes

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

[**Menu IWMPDVD. (VB et C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





