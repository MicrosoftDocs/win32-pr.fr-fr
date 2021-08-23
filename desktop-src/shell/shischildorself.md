---
UID: ''
title: SHIsChildOrSelf fonction)
description: Compare si une fenêtre est égale à, un enfant ou un descendant de, une deuxième fenêtre.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2d8eaab0f17647a6f548a0243199073baef074c88dad6a3f7100cfbca1a02be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941329"
---
# <a name="shischildorself-function"></a>SHIsChildOrSelf fonction)

## <a name="description"></a>Description

\[cette fonction est disponible par le biais de Windows XP et Windows Server 2003.
Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Compare si une fenêtre est égale à, un enfant ou un descendant de, une deuxième fenêtre.

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a>Paramètres

### <a name="hwndparent-in"></a>hwndParent [in]

Type : **HWND**

Handle de la première fenêtre.

### <a name="hwnd-in"></a>HWND [in]

Type : **HWND**

Handle d’une fenêtre à tester par rapport à *hwndParent*.

## <a name="returns"></a>Retours

Type : **HRESULT**

Retourne **S_OK** si la fenêtre spécifiée par *HWND* est égale à, un enfant de ou un descendant de la fenêtre spécifiée par *hwndParent*.
Retourne **S_FALSE** si la fenêtre spécifiée par HWND n’est pas égale à, pas un enfant de, et pas un descendant de la fenêtre spécifiée par *hwndParent*.
La valeur de retour n’est pas définie si l’un des handles de fenêtre n’est pas valide.

## <a name="remarks"></a>Remarques

## <a name="see-also"></a>Voir aussi

[IsChild,](/windows/desktop/api/winuser/nf-winuser-ischild)
