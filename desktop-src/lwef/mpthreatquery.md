---
title: MpThreatQuery, fonction (MpClient. h)
description: Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpThreatQuery
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510955"
---
# <a name="mpthreatquery-function"></a>MpThreatQuery fonction)

Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*ThreatID* \[ dans\]
</dt> <dd>

Type : **\_ ID MPTHREAT**

Identificateur de menace pour lequel des informations sont demandées.

</dd> <dt>

*ppThreatInfo* \[ à\]
</dt> <dd>

Type : **PMPTHREAT \_ info \** _

Retourne un pointeur vers une structure d’informations sur les menaces, [_ *MPTHREAT \_ info* *](mpthreat-info.md). La structure contient des informations telles que l’ID de menace, le nom et la gravité.

</dd> <dt>

*ppThreatLocalizedInfo* \[ out, facultatif\]
</dt> <dd>

Type : **PMPTHREAT \_ \_ informations \* localisées* _

Retourne un pointeur vers une structure contenant des informations localisées sur la menace. Vous pouvez passer _ *null** si vous n’êtes pas intéressé par les informations localisées relatives à la menace. Consultez [**\_ \_ informations localisées MPTHREAT**](mpthreat-localized-info.md).

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

[**\_informations MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**\_informations localisées \_ MPTHREAT**](mpthreat-localized-info.md)
</dt> </dl>

 

 





