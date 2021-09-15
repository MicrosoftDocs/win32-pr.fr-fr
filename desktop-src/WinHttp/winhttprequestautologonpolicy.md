---
description: Comprend les paramètres possibles pour la stratégie d’ouverture de session automatique.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Énumération WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403597"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>Énumération WinHttpRequestAutoLogonPolicy

L’énumération **WinHttpRequestAutoLogonPolicy** comprend des paramètres possibles pour la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ toujours**
</dt> <dd>

Une ouverture de session authentifiée, à l’aide des informations d’identification par défaut, est effectuée pour toutes les demandes.

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**
</dt> <dd>

Une ouverture de session authentifiée, à l’aide des informations d’identification par défaut, est exécutée uniquement pour les demandes sur l’intranet local. L’intranet local est considéré comme n’importe quel serveur de la liste de contournement du proxy dans la configuration du proxy actuel.

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ jamais**
</dt> <dd>

L’authentification n’est pas utilisée automatiquement.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour définir la stratégie d’ouverture de session automatique, appelez la méthode [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) et spécifiez l’une des constantes précédentes.

> [!Note]  
> pour Windows XP et Windows 2000, consultez la section [configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional avec les \[ applications de bureau SP3 uniquement\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows 2000 server avec des \[ applications de bureau SP3 uniquement\]<br/>         |
| Composant redistribuable<br/>          | WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.<br/> |
| MIDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Versions de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




