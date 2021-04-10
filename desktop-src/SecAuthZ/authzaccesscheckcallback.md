---
description: Fonction définie par l’application qui gère les entrées de contrôle d’accès (ACE) de rappel au cours d’une vérification d’accès.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: AuthzAccessCheckCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211084"
---
# <a name="authzaccesscheckcallback-callback-function"></a>AuthzAccessCheckCallback fonction de rappel

La fonction **AuthzAccessCheckCallback** est une fonction définie par l’application qui gère les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de rappel au cours d’une vérification d’accès. **AuthzAccessCheckCallback** est un espace réservé pour le nom de la fonction définie par l’application. L’application inscrit ce rappel en appelant [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hAuthzClientContext* \[ dans\]
</dt> <dd>

Handle d’un contexte client.

</dd> <dt>

*rythme* \[ dans\]
</dt> <dd>

Pointeur vers l’entrée du contrôle d’accès à évaluer pour l’inclusion dans l’appel à la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

</dd> <dt>

*pArgs* \[ dans, facultatif\]
</dt> <dd>

Données passées dans le paramètre *DynamicGroupArgs* de l’appel à [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) ou [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).

</dd> <dt>

*pbAceApplicable* \[ in, out\]
</dt> <dd>

Pointeur vers une variable booléenne qui reçoit les résultats de l’évaluation de la logique définie par l’application.

Les résultats sont **vrais** si la logique détermine que l’entrée du contrôle d’accès est applicable et sera incluse dans l’appel à [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); dans le cas contraire, les résultats sont **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la fonction retourne **true**.

Si la fonction ne peut pas effectuer l’évaluation, elle retourne **false**. Utilisez [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour renvoyer une erreur à la fonction de vérification d’accès.

## <a name="remarks"></a>Notes

Les variables d’attribut de sécurité doivent être présentes dans le contexte client si elles sont référencées dans une expression conditionnelle ; sinon, le terme d’expression conditionnelle qui les référence prend la valeur Unknown.

Pour plus d’informations, consultez la vue d’ensemble du [fonctionnement de AccessCheck](how-dacls-control-access-to-an-object.md) et de la [stratégie d’autorisation centralisée](centralized-authorization-policy.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                   |
| Composant redistribuable<br/>          | Pack des outils d’administration Windows Server 2003 sur Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de base Access Control](authorization-functions.md)
</dt> <dt>

[Stratégie d’autorisation centralisée](centralized-authorization-policy.md)
</dt> <dt>

[Fonctionnement de AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

