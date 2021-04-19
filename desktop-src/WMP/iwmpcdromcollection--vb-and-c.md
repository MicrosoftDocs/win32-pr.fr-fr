---
title: Interface IWMPCdromCollection (VB et C) (WMP. h)
description: Fournit un moyen d’organiser et d’accéder à une collection de lecteurs de CD ou DVD. L’interface IWMPCdromCollection expose la propriété suivante.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- IWMPCdromCollection (VB et C) interface Windows Media Player
- Interface IWMPCdromCollection (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fbc9c053c186b6d542e201f7bee5d2331b649
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530982"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a>Interface IWMPCdromCollection (VB et C#)

Fournit un moyen d’organiser et d’accéder à une collection de lecteurs de CD ou DVD.

L’interface **IWMPCdromCollection** expose la propriété suivante.

## <a name="members"></a>Membres

L’interface **IWMPCdromCollection (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPCdromCollection (VB et C#)** possède ces méthodes.



| Méthode                                                                                                     | Description                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**getByDriveSpecifier**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | Retourne une interface **IWMPCdrom** associée à une lettre de lecteur particulière.<br/> |
| [**Élément**](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | Retourne une interface **IWMPCdrom** à l’index donné.<br/>                        |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPCdromCollection (VB et C#)** a ces propriétés.



| Propriété                                                                                  | Type d’accès          | Description                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [**count**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient le nombre de lecteurs de CD et de DVD disponibles sur le système.<br/> |



 

Procurez-vous une interface **IWMPCdromCollection** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**cdromCollection**](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPCdrom (VB et C#)**](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





