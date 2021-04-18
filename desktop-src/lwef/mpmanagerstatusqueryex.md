---
title: MpManagerStatusQueryEx, fonction (MpClient. h)
description: Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants. | MpManagerStatusQueryEx, fonction (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerStatusQueryEx
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522932"
---
# <a name="mpmanagerstatusqueryex-function"></a>MpManagerStatusQueryEx fonction)

Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*dwFlag* \[ dans\]
</dt> <dd>

Type : **DWORD**

Contrôle les informations de requête retournées. Certaines informations sont coûteuses et peuvent ne pas être nécessaires.



| Valeur                                                                                                                                                                                                         | Signification                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**indicateurs de requête d’État du pack d' \_ état \_ \_ \_ aucun**</dt> </dl>       | Par défaut.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**\_indicateur de requête d’État MP \_ \_ \_ nostate**</dt> </dl> | Ne pas interroger les informations d’État.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ à\]
</dt> <dd>

Type : **PMPSTATUS \_ info**

Pointeur vers une structure qui retourne les informations d’État relatives aux dernières analyses, aux menaces actives et à l’état des différents composants. Consultez [**MPSTATUS \_ info**](mpstatus-info.md).

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_informations MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





