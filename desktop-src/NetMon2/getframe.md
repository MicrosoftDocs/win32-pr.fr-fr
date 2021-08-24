---
description: La fonction GetFrame retourne un handle à un frame donné dans une capture.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: GetFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5f6f992c0c61978e2de6f90755852c9e29d6ac51d7ae7f2405ef981ed695c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779249"
---
# <a name="getframe-function"></a>GetFrame fonction)

La fonction **GetFrame** retourne un handle à un frame donné dans une capture.

## <a name="syntax"></a>Syntaxe


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCapture* \[ dans\]
</dt> <dd>

Handle vers une capture. Pour obtenir le handle de capture, appelez la fonction [GetFrameCaptureHandle](getframecapturehandle.md) .

</dd> <dt>

*FrameNumber* \[ dans\]
</dt> <dd>

Nombre (de base zéro) du frame. Le numéro de la première trame dans une capture est égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un handle vers le frame.

Si la fonction échoue (autrement dit, si *hCapture* n’est pas valide ou si le numéro de frame est hors limites), la valeur de retour est **null**.

## <a name="remarks"></a>Remarques

Utilisez la fonction **GetFrame** pour obtenir le descripteur de frame nécessaire lors de la localisation des instances d’une propriété. Les fonctions utilisées pour localiser des instances de propriété sont des [FindPropertyInstance](findpropertyinstance.md) qui localisent la première instance et [FindPropertyInstanceRestart](findpropertyinstancerestart.md) qui localise l’instance suivante.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrame** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




