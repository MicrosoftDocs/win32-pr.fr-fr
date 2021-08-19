---
description: La fonction AuthzFreeCentralAccessPolicyCallback est une fonction définie par l’application qui libère de la mémoire allouée par la fonction AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: AuthzFreeCentralAccessPolicyCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f51903708bd3993e2837d65107798b1ff546c5857eff3bbed028ed4d6dda47f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783753"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>AuthzFreeCentralAccessPolicyCallback fonction de rappel

La fonction *AuthzFreeCentralAccessPolicyCallback* est une fonction définie par l’application qui libère de la mémoire allouée par la fonction [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) . *AuthzFreeCentralAccessPolicyCallback* est un espace réservé pour le nom de la fonction définie par l’application.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCentralAccessPolicy* \[ dans\]
</dt> <dd>

Pointeur vers la stratégie d’accès centralisée à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la fonction retourne **true**.

Si la fonction ne peut pas effectuer l’évaluation, elle retourne **false**. Utilisez [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour renvoyer une erreur à la fonction de vérification d’accès.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations d’initialisation authment \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
