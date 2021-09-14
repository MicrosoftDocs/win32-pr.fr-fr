---
title: Méthode INapClientManagement GetNapClientInfo (NapManagement. h)
description: Récupère des informations sur le client NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Méthode GetNapClientInfo NAP
- Méthode GetNapClientInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110685"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>INapClientManagement :: GetNapClientInfo, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetNapClientInfo** récupère des informations sur le client NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*isNapEnabled* \[ à\]
</dt> <dd>

Pointeur vers un booléen dont la valeur est **true** si la protection d’accès réseau est activée ; Sinon, elle a la valeur **false**.

</dd> <dt>

*clientName* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom du client.

</dd> <dt>

*clientDescription* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la description du client.

</dd> <dt>

*protocolVersion* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version du protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.



| Code de retour                                                                                         | Description                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | L’opération a réussi.<br/>                                   |
| <dl> <dt>**\_ACCESSDENIED E**</dt> </dl>      | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>       | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**RPC \_ E \_ déconnecté**</dt> </dl> | NapAgent n’est pas en cours d’exécution.<br/>                            |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





