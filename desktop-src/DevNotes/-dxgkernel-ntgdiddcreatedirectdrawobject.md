---
description: Crée une représentation côté noyau de l’objet Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: NtGdiDdCreateDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 6925932a6a400565ad942abbf845db591a9cb39dcad2559f1e3e8cb3951e51e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956688"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a>NtGdiDdCreateDirectDrawObject fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Crée une représentation côté noyau de l’objet Microsoft DirectDraw.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Tout périphérique d’affichage DC pour lequel l’objet DirectDraw doit être créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne un handle vers la représentation d’objet en mode noyau. Sinon, elle retourne la **valeur null**.

## <a name="remarks"></a>Remarques

Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques. Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.

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

[**DdCreateDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
