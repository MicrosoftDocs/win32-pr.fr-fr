---
title: INapSoHProcessor Initialize, méthode (NapProtocol. h)
description: Initialise le paquet de protocole et le système du processeur SoH. Cette méthode doit être appelée exactement une fois.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942128"
---
# <a name="inapsohprocessorinitialize-method"></a>INapSoHProcessor :: Initialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHProcessor :: Initialize** Initialise le paquet de protocole et le système du processeur SOH. Cette méthode doit être appelée exactement une fois.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SOH* \[ dans\]
</dt> <dd>

Pointeur vers le paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) à traiter.

</dd> <dt>

*isRequest* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui est **true** si le paquet est un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** s’il s’agit d’un **SoHResponse**.

</dd> <dt>

*ID* \[ sortant\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent SHA ou SHV qui a construit le paquet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**\_paquet NAP E \_ non valide \_**</dt> </dl> | Le paquet SoH n’est pas valide.<br/>                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





