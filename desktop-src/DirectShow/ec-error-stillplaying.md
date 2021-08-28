---
description: Une commande asynchrone pour exécuter le graphique a échoué.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82383c541f2ba5294cf4d45844f096ff510f25444ce87a54b956d0a777a7fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051779"
---
# <a name="ec_error_stillplaying"></a>\_erreur EC \_ STILLPLAYING

Une commande asynchrone pour exécuter le graphique a échoué.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Code d’échec de l’opération qui a échoué.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Si le gestionnaire de graphes de filtres émet une commande d’exécution asynchrone qui échoue, il envoie cet événement à l’application. Le graphique reste à l’État en cours d’exécution. L’état des filtres sous-jacents est indéterminé. Certains filtres sont peut-être en cours d’exécution, d’autres non.

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

 

 




