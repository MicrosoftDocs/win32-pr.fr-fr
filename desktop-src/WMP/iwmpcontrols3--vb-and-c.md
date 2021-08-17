---
title: interface IWMPControls3 (VB et C) (Wmp. h)
description: Fournit des propriétés et des méthodes pour la sélection et la prise en charge de la langue audio qui complètent l’interface IWMPControls2. En plus des propriétés et des méthodes héritées de IWMPControls2, l’interface IWMPControls3 expose les propriétés suivantes.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- interface IWMPControls3 (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPControls3 (VB et C), description
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2baf3f0b5f2bc4f2e4d0bfa5ccddd717c913aa30f5e24b5559eb527c910bcaf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135412"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>interface IWMPControls3 (VB et C#)

Fournit des propriétés et des méthodes pour la sélection et la prise en charge de la langue audio qui complètent l’interface **IWMPControls2** .

En plus des propriétés et des méthodes héritées de **IWMPControls2**, l’interface **IWMPControls3** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPControls3 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPControls3 (VB et C#)** possède ces méthodes.



| Méthode                                                                                                         | Description                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Retourne la description de la langue audio correspondant à l’index de base 1 spécifié.<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Retourne le LCID pour un index de langue audio spécifié.<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Retourne le nom de la langue audio avec le LCID spécifié.<br/>                                |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPControls3 (VB et C#)** a ces propriétés.



| Propriété                                                                                                              | Type d’accès           | Description                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Lecture seule<br/>  | Obtient le nombre de langues audio prises en charge. <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture. <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Lecture/écriture<br/> | Obtient ou définit l’index de base un qui correspond au langage audio pour la lecture. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Lecture/écriture<br/> | Obtient ou définit la position actuelle dans l’élément multimédia en cours à l’aide d’un format de code d’heure. Cette propriété prend actuellement en charge le code de temps SMPTE. <br/> |



 

Obtient une interface **IWMPControls3** en effectuant un cast de la valeur retournée par la propriété [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB et C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls2 (VB et C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





