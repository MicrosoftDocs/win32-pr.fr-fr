---
title: Interface IWMPCdromRip (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes pour gérer la copie ou l’extraction des pistes d’un CD audio. l’extraction d’un CD à l’aide de l’interface IWMPCdromRip a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- IWMPCdromRip (VB et C) interface Windows Media Player
- Interface IWMPCdromRip (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540471"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interface IWMPCdromRip (VB et C#)

Fournit des propriétés et des méthodes pour gérer la copie, ou l' *extraction*, des pistes d’un CD audio.

L’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media. Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur. Pour plus d’informations sur les préférences de l’utilisateur pour l’extraction de CD, consultez « extraction de musique à partir de CD » dans l’aide du lecteur Windows Media.

L’interface **IWMPCdromRip** expose les propriétés suivantes.

## <a name="members"></a>Membres

L’interface **IWMPCdromRip (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPCdromRip (VB et C#)** possède ces méthodes.



| Méthode                                                                 | Description                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Déchirure du CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Arrête le processus d’extraction de CD.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPCdromRip (VB et C#)** a ces propriétés.



| Propriété                                                                                | Type d’accès          | Description                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient la progression de l’extraction de CD comme pourcentage effectué.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Lecture seule<br/> | Obtient une valeur d’énumération qui indique l’état actuel du processus d’extraction.<br/> |



 

Procurez-vous une interface **IWMPCdromRip** en effectuant un cast de l’interface **IWMPCdrom** du CD que vous souhaitez extraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





