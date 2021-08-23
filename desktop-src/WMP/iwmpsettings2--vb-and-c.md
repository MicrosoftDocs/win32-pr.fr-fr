---
title: interface IWMPSettings2 (VB et C) (Wmp. h)
description: Fournit des propriétés et une méthode qui complètent l’interface IWMPSettings. En plus des propriétés et des méthodes héritées de IWMPSettings, l’interface IWMPSettings2 expose les propriétés suivantes.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- interface IWMPSettings2 (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPSettings2 (VB et C), description
topic_type:
- apiref
api_name:
- IWMPSettings2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e227cc255eee625df926031369ef8be0fe270e377b143adff2c3ed2d9ab0aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135352"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>interface IWMPSettings2 (VB et C#)

Fournit des propriétés et une méthode qui complètent l’interface **IWMPSettings** .

En plus des propriétés et des méthodes héritées de **IWMPSettings**, l’interface **IWMPSettings2** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPSettings2 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPSettings2 (VB et C#)** possède ces méthodes.



| Méthode                                                                                                   | Description                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Demande un niveau d’accès spécifié à la bibliothèque.<br/> |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPSettings2 (VB et C#)** a ces propriétés.



| Propriété                                                                                                    | Type d’accès          | Description                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut. <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Lecture seule<br/> | Obtient une valeur indiquant les autorisations actuellement accordées pour l’accès à la bibliothèque. <br/> |



 

Obtient une interface **IWMPSettings2** en effectuant un cast de la valeur retournée par la propriété **AxWindowsMediaPlayer. Settings** .



| Object                                                                   | Propriété                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Paramètres**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





