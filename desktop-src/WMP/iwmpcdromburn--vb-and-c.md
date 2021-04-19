---
title: Interface IWMPCdromBurn (VB et C) (WMP. h)
description: Fournit des propriétés et des méthodes pour gérer la création de CD audio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- IWMPCdromBurn (VB et C) interface Windows Media Player
- Interface IWMPCdromBurn (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdromBurn (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fe21a20194f57e4a8b52a3ba05032a07cb31f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534806"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>Interface IWMPCdromBurn (VB et C#)

Fournit des propriétés et des méthodes pour gérer la création de CD audio.

## <a name="members"></a>Membres

L’interface **IWMPCdromBurn (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IWMPCdromBurn (VB et C#)** possède ces méthodes.



| Méthode                                                                             | Description                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Efface le CD actuel.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Récupère la valeur de l’attribut spécifié pour le CD.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Fournit des informations sur le lecteur de CD et le support.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Met à jour les informations d’état de la sélection de gravure actuelle.<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Grave le CD.<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Arrête le processus de gravure de CD.<br/>                                 |



 

### <a name="properties"></a>Propriétés

L’interface **IWMPCdromBurn (VB et C#)** a ces propriétés.



| Propriété                                                                                    | Type d’accès          | Description                                                                 |
|:--------------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**burnFormat**](wmplibiwmpcdromburn-iwmpcdromburn-burnformat--vb-and-c.md)<br/>     | Lecture seule<br/> | Obtient une valeur qui indique le type de CD à graver.<br/>              |
| [**burnPlaylist**](wmplibiwmpcdromburn-iwmpcdromburn-burnplaylist--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient la sélection actuelle à graver sur le CD.<br/>                     |
| [**burnProgress**](wmplibiwmpcdromburn-iwmpcdromburn-burnprogress--vb-and-c.md)<br/> | Lecture seule<br/> | Obtient la progression de la gravure de CD comme pourcentage terminé.<br/>                |
| [**burnState**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)<br/>       | Lecture seule<br/> | Obtient une valeur d’énumération qui indique l’état d’avancement actuel.<br/> |
| [**noms**](wmplibiwmpcdromburn-iwmpcdromburn-label--vb-and-c.md)<br/>               | Lecture seule<br/> | Obtient la chaîne du nom du volume du CD.<br/>                                 |



 

Procurez-vous une interface **IWMPCdromBurn** en effectuant un cast de l’interface **IWMPCdrom** du CD que vous souhaitez graver.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





