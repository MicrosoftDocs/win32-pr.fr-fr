---
description: Le fichier source a été fermé en raison d’un événement inattendu. Par exemple, le serveur réseau a été arrêté.
ms.assetid: 1bbedf76-e840-4ec6-b3b2-c7e7dee47cf5
title: EC_FILE_CLOSED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b345bb364504a285b384a89f1fc6987a61ffba998608df0185f7871264d466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748889"
---
# <a name="ec_file_closed"></a>\_fichier EC \_ fermé

Le fichier source a été fermé en raison d’un événement inattendu. Par exemple, le serveur réseau a été arrêté.

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

Aucun.

## <a name="remarks"></a>Notes

le filtre de Source du média Windows hérité envoie cet événement. Les nouveaux filtres ne doivent pas envoyer cet événement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




