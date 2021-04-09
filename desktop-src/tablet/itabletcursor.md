---
description: Représente un objet stylet.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interface ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868682"
---
# <a name="itabletcursor-interface"></a>Interface ITabletCursor

Représente un objet stylet.

## <a name="members"></a>Membres

L’interface **ITabletCursor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITabletCursor** possède ces méthodes.



| Méthode                                                 | Description                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetButton**](itabletcursor-getbutton.md)           | Récupère l’objet bouton spécifié à partir d’un stylet de tablette.<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | Récupère le nombre de boutons sur le stylet de tablette.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Récupère l’identificateur du stylet.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Récupère le nom du stylet du Tablet PC.<br/>                    |
| [**IsInverted**](itabletcursor-isinverted.md)         | Indique si le stylet est à l’envers.<br/>                     |



 

## <a name="remarks"></a>Notes

N'utilisez pas cette interface.

Le code suivant décrit comment l’interface **ITabletCursor** est définie.

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

