---
title: interface IWMPCdromCollection (VB et C) (Wmp. h)
description: Fournit un moyen d’organiser et d’accéder à une collection de lecteurs de CD ou DVD. L’interface IWMPCdromCollection expose la propriété suivante.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- interface IWMPCdromCollection (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPCdromCollection (VB et C), description
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
ms.openlocfilehash: c935d4875307c7712036ed51304996028db6ba2a88fc1d5e54c77b7948c72252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119298"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a>interface IWMPCdromCollection (VB et C#)

Fournit un moyen d’organiser et d’accéder à une collection de lecteurs de CD ou DVD.

L’interface **IWMPCdromCollection** expose la propriété suivante.

## <a name="members"></a>Membres

l’interface **IWMPCdromCollection (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPCdromCollection (VB et C#)** possède ces méthodes.



| Méthode                                                                                                     | Description                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**getByDriveSpecifier**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | Retourne une interface **IWMPCdrom** associée à une lettre de lecteur particulière.<br/> |
| [**Élément**](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | Retourne une interface **IWMPCdrom** à l’index donné.<br/>                        |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPCdromCollection (VB et C#)** a ces propriétés.



| Propriété                                                                                  | Type d’accès          | Description                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [**saut**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient le nombre de lecteurs de CD et de DVD disponibles sur le système.<br/> |



 

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

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPCdrom (VB et C#)**](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





