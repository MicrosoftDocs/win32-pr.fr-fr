---
title: Message WM_DDE_POKE (DDE. h)
description: une application cliente de échange dynamique de données (dde) publie un message de l’application de \_ \_ serveur de publication dde dans une application de serveur dde.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE des données de message Exchange
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520860"
---
# <a name="wm_dde_poke-message"></a>Message d’échange de messages de l' \_ échange WM \_

une application cliente de échange dynamique de données (dde) publie un message de l’application de serveur de publication dde dans une application de serveur dde. **\_ \_** Un client utilise ce message pour demander au serveur d’accepter un élément de données non sollicité. Le serveur doit répondre avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE qui indique s’il a accepté l’élément de données.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre client qui publie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible est un handle vers un objet mémoire global contenant une structure [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) avec les données et des informations supplémentaires.

Le mot de poids fort contient un atome global qui identifie l’élément de données pour lequel les données ou la notification sont envoyées.

</dd> </dl>

## <a name="remarks"></a>Notes

### <a name="posting"></a>Publication

L’application cliente doit allouer de la mémoire pour l’objet de mémoire globale à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . L’application cliente doit supprimer l’objet si l’une des conditions suivantes est remplie :

-   L’application serveur répond avec un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif.
-   Le membre **fRelease** a la **valeur false**, mais l’application serveur répond avec un [**\_ \_ accusé**](wm-dde-ack.md)de réception DDE positif ou négatif.

L’application cliente doit créer Atom à l’aide de la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

L’application cliente doit créer ou réutiliser le paramètre de la fonction *lParam* de l' **échange de liaison ( \_ DDE \_ ) WM** en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

### <a name="receiving"></a>Réception

L’application serveur doit envoyer le message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour répondre positivement ou négativement. Lors de la publication d’un accusé de réception **\_ DDE DDE \_**, le serveur peut réutiliser l’Atom ou le supprimer et en créer un nouveau.

Le serveur doit créer ou réutiliser le paramètre [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Pour libérer l’objet mémoire globale, le serveur doit appeler la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . En outre, si le format de données est [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) ou **CF \_ MetaFilePict**, le serveur doit également appeler [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) avec le descripteur de métafichier incorporé. Ces deux formats ont un niveau supplémentaire d’indirection ; autrement dit, une application doit verrouiller l’objet pour obtenir un pointeur vers un handle, puis verrouiller ce handle pour obtenir un pointeur vers une structure [**MetaFilePict**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) et enfin appeler **DeleteMetaFile** avec le handle à partir du membre **hMF** de la structure **MetaFilePict** .

Pour libérer l’objet, le serveur doit appeler la fonction [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Dde. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 

