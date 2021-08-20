---
title: IWMPCdromBurn, méthode d’effacement
description: La méthode Erase efface le CD actuel.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- méthode erase Lecteur Windows Media
- erase, méthode Lecteur Windows Media, IWMPCdromBurn, interface
- Lecteur Windows Media de l’interface IWMPCdromBurn, méthode erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356b7bcdd332198c40760860e69741e76e0e993b6b47b3c5a5ff207d3d55bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116332"
---
# <a name="iwmpcdromburnerase-method"></a>IWMPCdromBurn :: Erase, méthode

La méthode **Erase** efface le CD actuel.

## <a name="syntax"></a>Syntaxe


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode ne fonctionne pas si le disque du lecteur n’est pas réinscriptible. Utilisez [IWMPCdromBurn. isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) pour déterminer si un CD peut être effacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media 11.<br/>                                                                                    |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





