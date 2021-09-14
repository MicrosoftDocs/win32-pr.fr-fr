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
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119265"
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

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un handle vers le frame.

Si la fonction échoue (autrement dit, si *hCapture* n’est pas valide ou si le numéro de frame est hors limites), la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Utilisez la fonction **GetFrame** pour obtenir le descripteur de frame nécessaire lors de la localisation des instances d’une propriété. Les fonctions utilisées pour localiser des instances de propriété sont des [FindPropertyInstance](findpropertyinstance.md) qui localisent la première instance et [FindPropertyInstanceRestart](findpropertyinstancerestart.md) qui localise l’instance suivante.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrame** .

## <a name="requirements"></a>Spécifications



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

 

 




