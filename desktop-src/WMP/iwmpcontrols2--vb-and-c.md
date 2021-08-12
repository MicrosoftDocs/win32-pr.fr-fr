---
title: IWMPControls2 (VB et C), interface (Wmp.h)
description: Fournit une méthode qui complète l’interface IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- interface IWMPControls2 (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPControls2 (VB et C), description
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9757471526eb385168a10c505254b5a418ea7f9811576de95266c06817c73109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575919"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>interface IWMPControls2 (VB et C#)

Fournit une méthode qui complète l’interface [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .

## <a name="members"></a>Membres

l’interface **IWMPControls2 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

l’interface **IWMPControls2 (VB et C#)** possède ces méthodes.



| Méthode                                                           | Description                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**première**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Déplace l’élément de média vidéo actuel vers le cadre suivant ou le frame précédent et gèle la lecture.<br/> |



 

L’exemple de code suivant montre comment accéder à une interface [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) . L’exemple de code convertit la valeur [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que la propriété [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) retourne à une valeur **IWMPControls2** .

Pour **C#**:


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Pour **VB**:


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls3 (VB et C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





