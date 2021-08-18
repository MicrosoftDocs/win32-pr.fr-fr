---
description: Définit des méthodes qui gèrent les événements de l’interface ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interface ITabletEventSink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a1a773f7b4e08a718c419de2d51c0ff3bd9bba551267188b12889b9ec99d4ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716458"
---
# <a name="itableteventsink-interface"></a>Interface ITabletEventSink

Définit des méthodes qui gèrent les événements de l' [**interface ITablet**](itablet.md) .

## <a name="members"></a>Membres

L’interface **ITabletEventSink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletEventSink** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITabletEventSink** possède ces méthodes.



| Méthode                                                        | Description                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Se produit lors de la création d’un nouveau contexte de tablette.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Se produit lorsqu’un contexte de tablette est en cours de destruction.<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | Se produit lorsque l’info-bulle du stylet contacte la surface de tablette numérique.<br/>                    |
| [**CursorInRange**](itableteventsink-cursorinrange.md)       | Se produit lorsqu’un stylet est dans la plage de détection du digitaliseur.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Se produit lorsque le curseur se déplace sur le digitaliseur de tablette.<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | Se produit lorsqu’un nouveau stylet est ajouté au système.<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | Se produit lorsque le stylet quitte la plage de détection physique (proximité) de la tablette.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Se produit lorsque l’utilisateur a relâché le stylet à partir de la surface du digitaliseur de tablette.<br/>         |
| [**Paquets**](itableteventsink-packets.md)                   | Se produit lorsque le stylet se déplace sur le digitaliseur.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Se produit lorsqu’un événement système est disponible.<br/>                                              |



 

## <a name="remarks"></a>Remarques

Les développeurs ne doivent pas utiliser cette interface.

Le code suivant illustre la définition de l’interface **ITabletEventSink** .

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

