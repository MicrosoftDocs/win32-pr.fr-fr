---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core. h)
description: Crée un objet de fabrique qui est utilisé pour la création suivante d’objets DWriteCore individuels.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882136"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>DWriteCoreCreateFactory, fonction (dwrite_core. h)

Crée un objet de fabrique qui est utilisé pour la création suivante d’objets DWriteCore individuels.

> [!IMPORTANT]
> Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes. Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Syntaxe
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>Paramètres

`factoryType`

Type : <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

Valeur qui spécifie si l’objet de fabrique sera partagé, isolé ou restreint.

`iid`

Type : <b>REFIID</b>

Valeur GUID qui identifie l’interface de fabrique DirectWrite, telle que __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).

`factory`

Type : <b>IUnknown * *</b>

Adresse d’un pointeur vers l’objet de fabrique DirectWrite nouvellement créé.

## <a name="return-value"></a>Valeur renvoyée

Type : <b>HRESULT</b>

Si cette méthode est réussie, elle retourne <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Sinon, elle retourne un code d’erreur <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Exemples

Consultez la rubrique [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Remarques

Elle fonctionne de la même façon que la fonction [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportée par la version système de DirectWrite. La fonction DWriteCore a un nom différent pour éviter toute ambiguïté.

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, réunion de projet (applications Win32) |
| **En-tête** | DWrite. h (inclure dwrite_core. h) |
