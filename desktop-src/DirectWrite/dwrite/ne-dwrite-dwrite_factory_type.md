---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Spécifie le type d’objet de fabrique DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 51cfbb274d681bb35b806f49aef13cc4a220ee26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550304"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>Énumération DWRITE_FACTORY_TYPE (DWRITE. h)

Spécifie le type d’objet de fabrique DirectWrite.

> [!IMPORTANT]
> Cette API est disponible dans le cadre de l’implémentation DWriteCore de [DirectWrite](../direct-write-portal.md). DWriteCore est une forme de DirectWrite qui s’exécute sur les versions de Windows jusqu’à Windows 8, et qui vous permet de l’utiliser sur plusieurs plateformes. Pour plus d’informations et pour obtenir des exemples de code, consultez [vue d’ensemble de DWriteCore](../dwritecore-overview.md).

## <a name="syntax"></a>Syntaxe
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a>Constantes

| Nom | Description |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Indique que la fabrique DirectWrite est une fabrique partagée et qu’elle permet la réutilisation des données de police mises en cache sur plusieurs composants in-process. De telles fabriques tirent également parti des composants de mise en cache des polices inter-processus pour de meilleures performances. |
| DWRITE_FACTORY_TYPE_ISOLATED | Indique que l’objet de fabrique DirectWrite est isolé. Les objets créés à partir de la fabrique isolée n’interagissent pas avec l’État DirectWrite interne à partir d’autres composants. |
| DWRITE_FACTORY_TYPE_ISOLATED2 | Indique que l’objet de fabrique DirectWrite est limité. Les objets créés à partir d’une fabrique limitée n’utilisent pas et ne modifient pas l’état interne ni les données mises en cache utilisées par d’autres fabriques. En outre, la collection de polices système contient uniquement des polices bien connues.|

## <a name="examples"></a>Exemples

Consultez la rubrique [vue d’ensemble de DWriteCore](../dwritecore-overview.md) et l’exemple d’application [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Remarques

Un objet de fabrique DirectWrite contient des informations sur son état interne, telles que l’inscription du chargeur de polices et les données de police mises en cache. Dans la plupart des cas, vous devez utiliser l’objet de fabrique partagée, car il permet à plusieurs composants qui utilisent DirectWrite de partager des informations d’État DirectWrite internes, réduisant ainsi l’utilisation de la mémoire. Toutefois, dans certains cas, il est souhaitable de réduire l’impact d’un composant sur le reste du processus, par exemple un plug-in à partir d’une source non fiable, en le sandboxant et en l’isolant du reste des composants de processus. Dans ce cas, vous devez utiliser une fabrique isolée pour le composant sandbox.

Une fabrique restreinte est plus verrouillée qu’une fabrique isolée. Il n’interagit d’aucune manière avec un cache de polices interprocessus ou persistant. En outre, la collection de polices système retournée par cette fabrique comprend uniquement des polices bien connues. Si vous transmettez **DWRITE_FACTORY_TYPE_ISOLATED2** à une version de DWRITE antérieure à DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) retourne **E_INVALIDARG**.

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, réunion de projet (applications Win32) |
| **En-tête** | DWrite. h (inclure dwrite_core. h) |