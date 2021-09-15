---
title: Méthode INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Récupère des informations sur le serveur NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Méthode GetNapServerInfo NAP
- Méthode GetNapServerInfo NAP, interface INapServerInfo
- INapServerInfo interface NAP, méthode GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413777"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>INapServerInfo :: GetNapServerInfo, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapServerInfo :: GetNapServerInfo** récupère des informations sur le serveur NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom du serveur.

</dd> <dt>

*serverDescription* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la description du serveur.

</dd> <dt>

*protocolVersion* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version du protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                               |
| En-tête<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





