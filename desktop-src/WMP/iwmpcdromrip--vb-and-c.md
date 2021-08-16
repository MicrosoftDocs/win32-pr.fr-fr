---
title: interface IWMPCdromRip (VB et C) (Wmp. h)
description: fournit des propriétés et des méthodes pour gérer la copie ou l’extraction des pistes d’un cd audio. l’extraction d’un cd à l’aide de l’interface IWMPCdromRip a le même effet que l’extraction de musique à l’aide de l’interface utilisateur Lecteur Windows Media.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- interface IWMPCdromRip (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPCdromRip (VB et C), description
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
ms.openlocfilehash: 98a418f71ad8605e81115fa9ef1a45488a6830db94c260ef60aa0d991724d80a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747935"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>interface IWMPCdromRip (VB et C#)

Fournit des propriétés et des méthodes pour gérer la copie, ou l' *extraction*, des pistes d’un CD audio.

l’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur Lecteur Windows Media. Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur. pour plus d’informations sur les préférences de l’utilisateur pour l’extraction de cd, consultez « extraction de musique à partir de cd » dans l’aide de Lecteur Windows Media.

L’interface **IWMPCdromRip** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPCdromRip (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPCdromRip (VB et C#)** possède ces méthodes.



| Méthode                                                                 | Description                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Déchirure du CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Arrête le processus d’extraction de CD.<br/> |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPCdromRip (VB et C#)** a ces propriétés.



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

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





