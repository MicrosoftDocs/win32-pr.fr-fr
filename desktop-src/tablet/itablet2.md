---
description: Étend l’interface ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interface ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0df1114f5808e5fd08a1a2dbe00ccfb451eaa7096c978d3f4d454e508c0a2fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717348"
---
# <a name="itablet2-interface"></a>Interface ITablet2

Étend l' [**interface ITablet**](itablet.md).

## <a name="members"></a>Membres

L’interface **ITablet2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITablet2** possède ces méthodes.



| Méthode                                          | Description                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | Retourne le type de périphérique matériel que l’objet tablette représente, par exemple Mouse, Pen ou Touch.<br/> |



 

## <a name="remarks"></a>Remarques

cette interface a été introduite dans Windows Vista.

Les développeurs ne doivent pas utiliser cette interface.

Le code suivant décrit comment l’interface **ITablet2** est définie.

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

