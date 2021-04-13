---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, qui peut être utilisé pour le rendu des glyphes.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211191"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>Interface IDWriteBitmapRenderTarget2 (dwrite_3. h)

Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, qui peut être utilisé pour le rendu des glyphes.

> [!IMPORTANT]
> Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes. Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="inheritance"></a>Héritage

L’interface **IDWriteBitmapRenderTarget2** hérite de [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).

## <a name="methods"></a>Méthodes

L’interface **IDWriteBitmapRenderTarget2** possède ces méthodes.

| Méthode | Description |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2::GetBitmapData](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | Récupère les données de pixels d’une cible de rendu bitmap. |

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, projet Réunion 0,1 version préliminaire [applications Win32] |
| **En-tête** | dwrite_3. h (inclure dwrite_core. h) |