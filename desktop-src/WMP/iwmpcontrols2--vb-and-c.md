---
title: IWMPControls2 (VB et C), interface (Wmp.h)
description: Fournit une méthode qui complète l’interface IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB et C) interface Windows Media Player
- Interface IWMPControls2 (VB et C), le lecteur Windows Media, décrit
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
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538107"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>Interface IWMPControls2 (VB et C#)

Fournit une méthode qui complète l’interface [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .

## <a name="members"></a>Membres

L’interface **IWMPControls2 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMPControls2 (VB et C#)** possède ces méthodes.



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

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls3 (VB et C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





