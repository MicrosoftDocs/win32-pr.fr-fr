---
description: Représente des informations générales sur un bouton sur un appareil de stylet.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interface ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319722"
---
# <a name="itabletcursorbutton-interface"></a>Interface ITabletCursorButton

Représente des informations générales sur un bouton sur un appareil de stylet.

## <a name="members"></a>Membres

L’interface **ITabletCursorButton** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursorButton** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITabletCursorButton** possède ces méthodes.



| Méthode                                         | Description                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Récupère l’identificateur unique du bouton du stylet.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Récupère le nom du bouton du stylet.<br/>              |



 

## <a name="remarks"></a>Notes

Les développeurs ne doivent pas utiliser cette interface.

Le code suivant illustre la définition de l’interface **ITabletCursorButton** .

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

