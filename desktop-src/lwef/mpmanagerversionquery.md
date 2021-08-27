---
title: MpManagerVersionQuery, fonction (MpClient. h)
description: Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpManagerVersionQuery
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6407f36650b699f6bcdc9cbdd832ff2db38f68e9db758411d42aa5e81564ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114539"
---
# <a name="mpmanagerversionquery-function"></a>MpManagerVersionQuery fonction)

Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*pVersionInfo* \[ à\]
</dt> <dd>

Type : **PMPVERSION \_ info**

Pointeur vers une structure qui contient des informations de version sur différents composants du gestionnaire de protection contre les programmes malveillants. Consultez [**MPVERSION \_ info**](mpversion-info.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec. L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_informations MPVERSION**](mpversion-info.md)
</dt> </dl>

 

 





