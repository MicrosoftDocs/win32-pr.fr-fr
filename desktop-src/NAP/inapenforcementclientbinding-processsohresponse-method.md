---
title: Méthode INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: Est utilisé par les clients de mise en œuvre pour traiter un SoHResponse chaque fois qu’ils reçoivent un objet blob de données SoHResponse à partir du serveur de mise en œuvre.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Méthode ProcessSoHResponse NAP
- Méthode ProcessSoHResponse NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519177"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>INapEnforcementClientBinding ::P méthode rocessSoHResponse

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapEnforcementClientBinding ::P rocesssohresponse** est utilisée par les clients de mise en œuvre pour traiter un SoHResponse chaque fois qu’ils reçoivent un objet blob de données SoHResponse du serveur d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*connexion* \[ dans\]
</dt> <dd>

Pointeur COM vers l’interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la connexion cliente. NapAgent ne contient pas de références à l’objet associé à cette interface après la fin de l’appel de méthode.

Vous devez utiliser une connexion précédemment établie pour le traitement des objets BLOB de données SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                             | Description                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'opération a réussi.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Aucune connexion n’a été créée précédemment sur le client de contrainte. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_paquet NAP E \_ non valide \_**</dt> </dl>  | Si cette valeur est renvoyée, le client de contrainte doit supprimer le paquet si le NapAgent retourne le \_ paquet NAP E \_ non valide \_ . Dans ce cas, l’application doit supposer que le serveur auquel elle est confrontée n’est pas compatible avec la protection d’accès réseau (NAP) et supprime la connexion de la liste active (par exemple, notifier le NapAgent d’un état de connexion).<br/> |
| <dl> <dt>**\_ID non \_ compatible NAP \_**</dt> </dl>   | Si cette valeur est retournée, elle indique que l’ID de corrélation dans le paquet SoH-Response ne correspond pas à la réponse SoH en suspens. Dans ce cas, l’application doit supprimer le paquet et attendre un autre paquet plus récent SoH-Response.<br/> Cela peut être dû à une réponse à un message de demande plus ancien.<br/>        |
| <dl> <dt>**NAP \_ E \_ non \_ initialisé**</dt> </dl> | L’application n’a pas été précédemment initialisée.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Notes

Le NapAgent interroge l’objet blob de données SoH-Response à partir de l’objet de connexion, le traite et définit la décision résultante (par exemple, accès complet/restreint, etc.) sur l’objet de connexion.

Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





