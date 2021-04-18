---
description: Envoyé lorsqu’une application utilise le filtre d’enregistreur ASF WM pour indexer Windows Media Video fichiers.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532859"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (DShow. h)

Envoyé lorsqu’une application utilise le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) pour indexer Windows Media Video fichiers.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Il peut s’agir de l’un des messages d' **\_ État WMT** suivants.



| Valeur                | Description              |
|----------------------|--------------------------|
| WMT \_ démarré         | L’indexation a commencé.      |
| WMT \_ fermé          | L’indexation est terminée.  |
| progression de l' \_ index WMT \_ | L’indexation est en cours. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *lParam1* a été \_ fermé par WMT ou si WMT \_ a démarré, *lParam2* est égal à zéro. Si *lParam1* est en \_ \_ cours d’index WMT, *lParam2* est une **valeur DWORD** qui spécifie la progression actuelle sous la forme d’un pourcentage de la taille totale du téléchargement.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




