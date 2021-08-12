---
title: interface IWMPCdromBurn (VB et C) (Wmp. h)
description: Fournit des propriétés et des méthodes pour gérer la création de CD audio.
ms.assetid: d98b243d-d6c2-4d85-8d5a-de49c62d0acf
keywords:
- interface IWMPCdromBurn (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPCdromBurn (VB et C), description
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
ms.openlocfilehash: 7731d5491e683c2a5d2e577c41dc96264c90f0d070538405d0fa3c3ea7283a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575957"
---
# <a name="iwmpcdromburn-vb-and-c-interface"></a>interface IWMPCdromBurn (VB et C#)

Fournit des propriétés et des méthodes pour gérer la création de CD audio.

## <a name="members"></a>Membres

l’interface **IWMPCdromBurn (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPCdromBurn (VB et C#)** possède ces méthodes.



| Méthode                                                                             | Description                                                              |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**erase**](wmplibiwmpcdromburn-iwmpcdromburn-erase--vb-and-c.md)                 | Efface le CD actuel.<br/>                                        |
| [**getItemInfo**](wmplibiwmpcdromburn-iwmpcdromburn-getiteminfo-iwmpcdromburn.md) | Récupère la valeur de l’attribut spécifié pour le CD.<br/>    |
| [**isAvailable**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)     | Fournit des informations sur le lecteur de CD et le support.<br/>            |
| [**refreshStatus**](wmplibiwmpcdromburn-iwmpcdromburn-refreshstatus--vb-and-c.md) | Met à jour les informations d’état de la sélection de gravure actuelle.<br/> |
| [**startBurn**](wmplibiwmpcdromburn-iwmpcdromburn-startburn--vb-and-c.md)         | Grave le CD.<br/>                                                 |
| [**stopBurn**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)       | Arrête le processus de gravure de CD.<br/>                                 |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPCdromBurn (VB et C#)** a ces propriétés.



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

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





