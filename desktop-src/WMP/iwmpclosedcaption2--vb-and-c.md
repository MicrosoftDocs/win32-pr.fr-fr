---
title: Interface IWMPClosedCaption2 (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes pour les sous-titres qui complètent l’interface IWMPClosedCaption. Outre les propriétés héritées de IWMPClosedCaption, l’interface IWMPClosedCaption2 expose les propriétés suivantes.
ms.assetid: e34ea819-dc1a-48f3-9e55-cf2217379ddb
keywords:
- IWMPClosedCaption2 (VB et C) interface Windows Media Player
- Interface IWMPClosedCaption2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPClosedCaption2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dbf81cef3734a6466b6fd177ccc87a38c5c7085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530525"
---
# <a name="iwmpclosedcaption2-vb-and-c-interface"></a>Interface IWMPClosedCaption2 (VB et C#)

Fournit des propriétés et des méthodes pour les sous-titres qui complètent l’interface **IWMPClosedCaption** .

Outre les propriétés héritées de **IWMPClosedCaption**, l’interface **IWMPClosedCaption2** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPClosedCaption2 (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPClosedCaption2 (VB et C#)** possède ces méthodes.



| Méthode                                                                                             | Description                                                                                       |
|:---------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| [**getSAMILangID**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangid--vb-and-c.md)       | Retourne l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel.<br/> |
| [**getSAMILangName**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)   | Retourne le nom d’une langue prise en charge par le fichier SAMI actuel.<br/>                     |
| [**getSAMIStyleName**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md) | Retourne le nom d’un style pris en charge par le fichier SAMI actuel.<br/>                        |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPClosedCaption2 (VB et C#)** a ces propriétés.



| Propriété                                                                                                | Type d’accès           | Description                                                                         |
|:--------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------|
| [**SAMILangCount**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-samilangcount--vb-and-c.md)<br/> | Lecture/écriture<br/> | Obtient ou définit le nombre de langues prises en charge par le fichier SAMI actuel.<br/> |
| [**SAMIStyleCount**](wmplibiwmpclosedcaption2-samistylecount.md)<br/>                            | Lecture/écriture<br/> | Obtient ou définit le nombre de styles pris en charge par le fichier SAMI actuel.<br/>    |



 

Obtient une interface **IWMPClosedCaption2** en effectuant un cast de la valeur retournée par la propriété [**AxWindowsMediaPlayer. closedCaption**](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB et C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> </dl>

 

 





