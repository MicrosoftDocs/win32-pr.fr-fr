---
title: MpManagerVersionQuery, fonction (MpClient. h)
description: Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerVersionQuery
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
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509336"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                    |
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

 

 





