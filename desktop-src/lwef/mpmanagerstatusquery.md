---
title: MpManagerStatusQuery, fonction (MpClient. h)
description: Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants. | MpManagerStatusQuery, fonction (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerStatusQuery
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321877"
---
# <a name="mpmanagerstatusquery-function"></a>MpManagerStatusQuery fonction)

\[**MpManagerStatusQuery** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]

Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
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

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**\_informations MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





