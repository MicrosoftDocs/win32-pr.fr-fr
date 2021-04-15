---
title: Méthode INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient. h)
description: Est utilisé pour obtenir des informations d’isolation sur le client.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Méthode GetIsolationInfoEx NAP
- Méthode GetIsolationInfoEx NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467062"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a>INapEnforcementClientConnection2 :: GetIsolationInfoEx, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientConnection2 :: GetIsolationInfoEx** est utilisée pour obtenir des informations d’isolation sur le client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*isolationInfo* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient la connectivité et les informations d’État étendues du client.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Ces informations sont définies par NapAgent après le traitement d’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) et ne doivent pas être définies par l’application.

L’algorithme SHA doit libérer la structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) en appelant [**FreeIsolationInfoEx**](freeisolationinfoex.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





