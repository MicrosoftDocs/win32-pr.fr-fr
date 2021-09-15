---
title: Méthode IWMPCdromBurn startBurn
description: La méthode startBurn grave le CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Lecteur Windows Media de la méthode startBurn
- méthode startBurn Lecteur Windows Media, interface IWMPCdromBurn
- Lecteur Windows Media de l’interface IWMPCdromBurn, méthode startBurn
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519853"
---
# <a name="iwmpcdromburnstartburn-method"></a>IWMPCdromBurn :: startBurn, méthode

La méthode **startBurn** grave le CD.

## <a name="syntax"></a>Syntaxe


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La valeur de **burnstate** doit être WmpbsReady ou wmpbsStopped avant d’appeler cette méthode.

Cette méthode ne fonctionne pas si le lecteur de CD n’est pas un graveur, ou si le disque du lecteur n’est pas accessible en écriture. Utilisez **isAvailable** pour déterminer si un CD peut être gravé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. burnState (VB et C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. isAvailable (VB et C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. stopBurn (VB et C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





