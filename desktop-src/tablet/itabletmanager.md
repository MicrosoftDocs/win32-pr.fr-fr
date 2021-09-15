---
description: Permet d’accéder à tous les tablettes attachées à l’ordinateur.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interface ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412263"
---
# <a name="itabletmanager-interface"></a>Interface ITabletManager

Permet d’accéder à tous les tablettes attachées à l’ordinateur.

## <a name="members"></a>Membres

L’interface **ITabletManager** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletManager** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITabletManager** possède ces méthodes.



| Méthode                                                  | Description                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | Récupère l’objet tablette spécifié.<br/>                  |
| [**GetTabletCount**](itabletmanager-gettabletcount.md) | Récupère le nombre de tablettes attachées au système.<br/> |



 

## <a name="remarks"></a>Notes

Les développeurs ne doivent pas utiliser cette interface.

Le code suivant illustre l’implémentation de l’interface **ITabletManager** .

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’ID de classe CLSID \_ TabletManagerS, puis appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur vers l' **interface ITabletManager**. Le \_ GUID TABLETMANAGERS CLSID est défini comme suit :

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

