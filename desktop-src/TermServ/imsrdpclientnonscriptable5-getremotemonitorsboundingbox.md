---
title: IMsRdpClientNonScriptable5 propriété GetRemoteMonitorsBoundingBox
description: Spécifie le rectangle englobant du moniteur distant.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GetRemoteMonitorsBoundingBox
- Services Bureau à distance de la propriété GetRemoteMonitorsBoundingBox, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942417"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a>IMsRdpClientNonScriptable5 :: GetRemoteMonitorsBoundingBox, propriété

Spécifie le rectangle englobant du moniteur distant.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a>Valeur de la propriété

Reçoit le bord gauche du rectangle.

Reçoit le bord supérieur du rectangle.

Reçoit le bord droit du rectangle.

Reçoit le bord inférieur du rectangle.

## <a name="remarks"></a>Notes

Toutes les coordonnées se trouvent dans des coordonnées d’écran virtuelles, qui sont relatives au coin supérieur gauche de l’écran principal. S’il ne s’agit pas du moniteur principal, une partie ou la totalité de ces valeurs peut être négative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





