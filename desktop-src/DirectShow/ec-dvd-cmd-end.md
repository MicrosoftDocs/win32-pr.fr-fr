---
description: Signale qu’une commande de navigateur de DVD particulière est terminée.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542223"
---
# <a name="ec_dvd_cmd_end"></a>fin de la commande de DVD de la EC \_ \_ \_

Signale qu’une commande de [navigateur de DVD](dvd-navigator-filter.md) particulière est terminée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificateur de commande. Transmettez ce paramètre à la méthode [**IDvdInfo2 :: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) pour récupérer un pointeur d’interface [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur **HRESULT** qui indique l’état de la commande.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet événement est déclenché uniquement si votre application définit l’indicateur \_ \_ \_ SendEvents de l’indicateur de commande de DVD dans une méthode [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) qui prend un indicateur d' [**\_ \_ indicateurs de cmd DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .

Cet événement est déclenché dans le domaine de titre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdevcode. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> <dt>

[Codes de notification des événements DVD](dvd-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Synchronisation des commandes de DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




