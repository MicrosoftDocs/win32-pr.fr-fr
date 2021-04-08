---
title: MpManagerOpen, fonction (MpClient. h)
description: Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerOpen
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743181"
---
# <a name="mpmanageropen-function"></a>MpManagerOpen fonction)

Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwReserved* \[ dans\]
</dt> <dd>

Type : **DWORD**

Réservé pour un usage futur. Doit avoir la valeur 0.

</dd> <dt>

*phMpHandle* \[ à\]
</dt> <dd>

Type : **PMPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**. Cet appel de fonction est garanti, même si un service anti-programme malveillant n’est pas en cours d’exécution.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec. L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





