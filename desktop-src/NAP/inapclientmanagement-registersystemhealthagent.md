---
title: Méthode INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Inscrit un SHA auprès du système NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Méthode RegisterSystemHealthAgent NAP
- Méthode RegisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466042"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>INapClientManagement :: RegisterSystemHealthAgent, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **RegisterSystemHealthAgent** inscrit un SHA auprès du système NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*agent* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription pour l’algorithme SHA.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | L’opération a réussi.<br/>                                   |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**\_ID en \_ conflit NAP \_ E**</dt> </dl> | Un SHA qui utilise cet ID est déjà inscrit.<br/>         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





