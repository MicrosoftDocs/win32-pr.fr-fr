---
description: Avertit l’application de la progression lors de l’ouverture d’un fichier réseau.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521715"
---
# <a name="ec_loadstatus"></a>\_LOADSTATUS EC

Avertit l’application de la progression lors de l’ouverture d’un fichier réseau.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Code d’état. Consultez la section Notes.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) et le filtre de [source Windows Media](windows-media-source-filter.md) hérité envoient cet événement. Le premier paramètre d’événement a l’une des valeurs suivantes.



| Valeur                        | Description                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ fermé       | Le filtre source a fermé le fichier.         |
| \_connexion am LOADSTATUS \_   | Le filtre source se connecte au serveur. |
| AM \_ LOADSTATUS \_ LOADINGDESCR | Non utilisé.                                      |
| AM \_ LOADSTATUS \_ LOADINGMCAST | Non utilisé                                       |
| \_recherche LOADSTATUS \_     | Le filtre source recherche les données demandées.  |
| AM \_ LOADSTATUS \_ ouvert         | Le filtre source a ouvert le fichier.         |
| \_ouverture de LOADSTATUS \_      | Le filtre source ouvre le fichier.         |



 

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

 

 




