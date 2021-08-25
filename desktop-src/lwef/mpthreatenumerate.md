---
title: MpThreatEnumerate, fonction (MpClient. h)
description: Retourne des informations sur la menace suivante dans la liste d’énumération. Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpThreatEnumerate
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9525ad44901bd62044721e634559e1c803b88b05e9250097d939b3a5a04d229a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943829"
---
# <a name="mpthreatenumerate-function"></a>MpThreatEnumerate fonction)

Retourne des informations sur la menace suivante dans la liste d’énumération. Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hThreatEnumHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle vers un contexte d’énumération des menaces retourné par [**MpThreatOpen**](mpthreatopen.md).

</dd> <dt>

*ppThreatInfo* \[ à\]
</dt> <dd>

Type : **PMPTHREAT \_ info \***

Retourne un pointeur vers une structure d’informations sur les menaces, [**MPTHREAT \_ info**](mpthreat-info.md). La structure contient des informations telles que l’ID de menace, le nom et la gravité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

S’il n’y a plus d’éléments à retourner, la valeur de retour est **\_ false**.

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

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**\_informations MPTHREAT**](mpthreat-info.md)
</dt> </dl>

 

 





