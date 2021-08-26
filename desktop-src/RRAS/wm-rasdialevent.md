---
title: Message WM_RASDIALEVENT (RAS. h)
description: Le système d’exploitation envoie un \_ message WM RASDIALEVENT à une procédure de fenêtre lorsqu’un changement d’événement d’État se produit pendant un processus de connexion RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT message RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093591ffe07ecbe662ca85306b74c34c670e1adbe51e2605b1f21faa20696c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024769"
---
# <a name="wm_rasdialevent-message"></a>\_Message WM RASDIALEVENT

Le système d’exploitation envoie un message **WM \_ RASDIALEVENT** à une procédure de fenêtre lorsqu’un changement d’événement d’État se produit pendant un processus de connexion RAS. Cela se produit lorsqu’une fenêtre a été spécifiée pour gérer les notifications de tels événements à l’aide du paramètre de *notificateur* de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Les deux paramètres de message sont équivalents aux paramètres des mêmes noms utilisés avec les fonctions de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) et [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Valeur de *wParam*. Équivalent au paramètre *rasconnstate* des fonctions de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) et [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Spécifie une valeur d’énumérateur [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) qui indique l’état que le processus de connexion d’accès à distance rasdial va entrer.

</dd> <dt>

*dwError* 
</dt> <dd>

Valeur de *lParam*. Équivalent au paramètre *dwError* des fonctions de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) et [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Une valeur différente de zéro indique l’erreur qui s’est produite, ou zéro si aucune erreur ne s’est produite.

[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) envoie ce message avec *dwError* défini à zéro lors de l’entrée à chaque État de connexion. Si une erreur se produit dans un État, le message est renvoyé pour l’État, cette fois avec une valeur *dwError* différente de zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Messages du service d’accès à distance](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

