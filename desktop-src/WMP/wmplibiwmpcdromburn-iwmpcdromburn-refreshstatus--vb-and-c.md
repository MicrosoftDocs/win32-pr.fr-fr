---
title: Méthode IWMPCdromBurn refreshStatus
description: La méthode refreshStatus met à jour les informations d’état de la sélection de gravure en cours.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- Lecteur Windows Media de la méthode refreshStatus
- méthode refreshStatus Lecteur Windows Media, interface IWMPCdromBurn
- Lecteur Windows Media de l’interface IWMPCdromBurn, méthode refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519857"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>IWMPCdromBurn :: refreshStatus, méthode

La méthode **refreshStatus** met à jour les informations d’état de la sélection de gravure en cours.

## <a name="syntax"></a>Syntaxe


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Vous devez appeler cette méthode après avoir créé ou modifié une sélection de gravure avant de lire les informations d’État ou de graver le CD. Vous pouvez tester si une actualisation est requise en obtenant la valeur de **burnState** et en vérifiant wmpbsRefreshStatusPending.

L’actualisation de l’État est une opération synchrone. Cela signifie qu’une longue période de temps peut s’écouler avant que cette méthode ne retourne si la sélection de gravure actuelle est volumineuse et contient de nombreuses modifications.

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

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





