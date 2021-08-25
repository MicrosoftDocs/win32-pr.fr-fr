---
description: Le graphique de filtre a changé d’État.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2b476c923f0b812196a5697444433ea0be65b8d3f46bd0388261b2a67a66881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905729"
---
# <a name="ec_state_change"></a>\_changement d’État EC \_

Le graphique de filtre a changé d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) , indiquant le nouvel État du graphique.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucune action par défaut. L’événement n’est pas envoyé à l’application.

> [!Note]  
> Cet événement peut se produire lorsque le graphique s’arrête. si vous remplacez l’action par défaut et que vous écoutez cet événement, vous devez veiller à ne pas traiter les événements après avoir libéré le filtre Graph Manager. Dans le cas contraire, votre application peut référencer un pointeur [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) non valide et se bloquer. Pour plus d’informations, consultez [réponse aux événements](responding-to-events.md).

 

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

 

 




