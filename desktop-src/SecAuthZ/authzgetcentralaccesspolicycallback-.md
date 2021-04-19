---
description: La fonction AuthzGetCentralAccessPolicyCallback est une fonction définie par l’application qui récupère la stratégie d’accès centralisée. AuthzGetCentralAccessPolicyCallback est un espace réservé pour le nom de la fonction définie par l’application.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: AuthzGetCentralAccessPolicyCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524742"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>AuthzGetCentralAccessPolicyCallback fonction de rappel

La fonction *AuthzGetCentralAccessPolicyCallback* est une fonction définie par l’application qui récupère la stratégie d’accès centralisée. *AuthzGetCentralAccessPolicyCallback* est un espace réservé pour le nom de la fonction définie par l’application.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hAuthzClientContext* \[ dans\]
</dt> <dd>

Handle vers le contexte client.

</dd> <dt>

*capid* \[ dans\]
</dt> <dd>

ID de la stratégie d’accès centralisée à récupérer.

</dd> <dt>

*pArgs* \[ dans, facultatif\]
</dt> <dd>

Arguments facultatifs passés à la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) via le membre **OptionalArguments** de la structure [**de \_ \_ demande d’accès auth**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ à\]
</dt> <dd>

Pointeur vers une valeur booléenne que le gestionnaire de ressources utilise pour indiquer si une stratégie d’accès centralisée doit être utilisée pendant l’évaluation de l’accès.

</dd> <dt>

*ppCentralAccessPolicy* \[ à\]
</dt> <dd>

Pointeur vers la stratégie d’accès centralisée (CAP) à utiliser pour l’évaluation de l’accès. Si cette valeur est **null**, l’extrémité par défaut est appliquée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la fonction retourne **true**.

Si la fonction ne peut pas effectuer l’évaluation, elle retourne **false**. Utilisez [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour renvoyer une erreur à la fonction de vérification d’accès.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                   |
| Composant redistribuable<br/>          | Pack des outils d’administration Windows Server 2003 sur Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_demande d’accès à auth. \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**\_informations d’initialisation authment \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

