---
description: L’utilisateur a terminé la lecture.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524023"
---
# <a name="ec_userabort"></a>\_USERABORT EC

L’utilisateur a terminé la lecture.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zéro.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun L’application doit décider d’arrêter ou non le graphique.

## <a name="remarks"></a>Notes

Ce code d’événement indique que l’utilisateur a terminé la lecture du graphique normal. Par exemple, les convertisseurs vidéo envoient cet événement si l’utilisateur ferme la fenêtre vidéo.

Après l’envoi de cet événement, le filtre doit rejeter tous les exemples et ne pas envoyer d’événements de [**\_ redessin EC**](ec-repaint.md) , jusqu’à ce que le filtre s’arrête et soit réinitialisé.

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

 

 




