---
description: Le graphique supprime des exemples, pour le contrôle de la qualité.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111109"
---
# <a name="ec_quality_change"></a>modification de la \_ qualité ce \_

Le graphique supprime des exemples, pour le contrôle de la qualité.

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

Un filtre envoie cet événement s’il supprime des exemples en réponse à un message de contrôle qualité. Il envoie l’événement uniquement lorsqu’il ajuste le niveau de qualité, et non pour chaque échantillon qu’il supprime. Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




