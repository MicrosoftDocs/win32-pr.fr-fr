---
description: Un filtre ne reçoit pas suffisamment de données.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537328"
---
# <a name="ec_starvation"></a>\_privation ce

Un filtre ne reçoit pas suffisamment de données.

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

L’événement n’est pas envoyé à l’application. Si le graphique de filtre est en cours d’exécution, le gestionnaire de graphes de filtre interrompt le graphique et attend la fin de la pause. Ensuite, il réexécute le graphique. Le filtre qui envoie l’événement ne doit pas terminer sa transition pour être suspendue jusqu’à ce qu’il dispose de suffisamment de données pour reprendre. Si le graphique de filtre n’est pas en cours d’exécution, le gestionnaire de graphes de filtres ignore cet événement.

## <a name="remarks"></a>Notes

Un analyseur ou un filtre source peut envoyer cet événement si l’arrivée de données est trop faible.

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

 

 




