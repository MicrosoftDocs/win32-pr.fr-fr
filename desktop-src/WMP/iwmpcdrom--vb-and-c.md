---
title: Interface IWMPCdrom (VB et C) (WMP. h)
description: Offre un moyen d’accéder à un CD ou un DVD dans son lecteur. L’interface IWMPCdrom expose les propriétés suivantes.
ms.assetid: 2748e64b-b9b7-489a-a6b5-21154aabd312
keywords:
- IWMPCdrom (VB et C) interface Windows Media Player
- Interface IWMPCdrom (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdrom (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036411c96b278023d87c37ad48f81e986b9dadcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528132"
---
# <a name="iwmpcdrom-vb-and-c-interface"></a>Interface IWMPCdrom (VB et C#)

Offre un moyen d’accéder à un CD ou un DVD dans son lecteur.

L’interface **IWMPCdrom** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPCdrom (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPCdrom (VB et C#)** possède ces méthodes.



| Méthode                                                     | Description                                     |
|:-----------------------------------------------------------|:------------------------------------------------|
| [**émission**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md) | Éjecte le CD ou DVD du lecteur.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPCdrom (VB et C#)** a ces propriétés.



| Propriété                                                                                | Type d’accès          | Description                                                                                                                                  |
|:----------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**driveSpecifier**](wmplibiwmpcdrom-iwmpcdrom-drivespecifier--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient la lettre du lecteur de CD ou de DVD.<br/>                                                                                                  |
| [**Playlist**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)<br/>             | Lecture seule<br/> | Obtient une interface [**IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) représentant les pistes sur un CD ou les entrées de titre au niveau de la racine d’un DVD.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





