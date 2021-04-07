---
description: Libère le contexte de périphérique (DC) créé précédemment pour l’objet surface Microsoft DirectDraw en mode noyau indiqué.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: NtGdiDdReleaseDC, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847033"
---
# <a name="ntgdiddreleasedc-function"></a>NtGdiDdReleaseDC fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Libère le contexte de périphérique (DC) créé précédemment pour l’objet surface Microsoft DirectDraw en mode noyau indiqué.

## <a name="syntax"></a>Syntaxe


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle vers l’objet de surface DirectDraw en mode noyau précédemment créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne la **valeur true**; Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Les applications qui doivent obtenir un contrôleur de réseau pour une surface DirectDraw peuvent utiliser [IDirectDrawSurface7 :: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), qui expose cette fonctionnalité de façon indépendante du système d’exploitation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des clients de bas niveau](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReleaseDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
