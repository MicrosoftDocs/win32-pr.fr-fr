---
description: Le graphique ouvre un fichier ou a fini d’ouvrir un fichier.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 436a48a90640577504871dfe835d6c81c398680ae070065189cb4031493e7fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079119"
---
# <a name="ec_opening_file"></a>\_fichier d’ouverture EC \_

Le graphique ouvre un fichier ou a fini d’ouvrir un fichier.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**True** si le graphique commence à ouvrir un fichier, ou **false** si le graphique n’ouvre plus le fichier.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Un filtre peut envoyer cet événement s’il consacre beaucoup de temps à ouvrir un fichier. (Par exemple, le fichier peut se trouver sur un réseau.) L’application peut utiliser cet événement pour ajuster son interface utilisateur.

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

 

 




