---
description: Fonction définie par l’application qui crée une liste d’identificateurs de sécurité (SID) qui s’appliquent à un client. AuthzComputeGroupsCallback est un espace réservé pour le nom de la fonction définie par l’application.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: AuthzComputeGroupsCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233442"
---
# <a name="authzcomputegroupscallback-callback-function"></a>AuthzComputeGroupsCallback fonction de rappel

La fonction **AuthzComputeGroupsCallback** est une fonction définie par l’application qui crée une liste d' [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui s’appliquent à un client. **AuthzComputeGroupsCallback** est un espace réservé pour le nom de la fonction définie par l’application.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hAuthzClientContext* \[ dans\]
</dt> <dd>

Handle d’un contexte client.

</dd> <dt>

*Arguments* \[ dans\]
</dt> <dd>

Données passées dans le paramètre *DynamicGroupArgs* d’un appel à la fonction [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)ou [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .

</dd> <dt>

*pSidAttrArray* \[ à\]
</dt> <dd>

Pointeur vers une variable pointeur qui reçoit l’adresse d’un tableau de sid et de structures d' [**\_ \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Ces structures représentent les groupes auxquels le client appartient.

</dd> <dt>

*pSidCount* \[ à\]
</dt> <dd>

Nombre de structures dans *pSidAttrArray*.

</dd> <dt>

*pRestrictedSidAttrArray* \[ à\]
</dt> <dd>

Pointeur vers une variable pointeur qui reçoit l’adresse d’un tableau de sid et de structures d' [**\_ \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Ces structures représentent les groupes dont le client est limité.

</dd> <dt>

*pRestrictedSidCount* \[ à\]
</dt> <dd>

Nombre de structures dans *pSidRestrictedAttrArray*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction retourne correctement une liste de sid, la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Les applications peuvent également ajouter des SID au contexte client en appelant [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).

Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                   |
| Composant redistribuable<br/>          | Windows Pack des outils d’Administration du serveur 2003 sur Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de base Access Control](authorization-functions.md)
</dt> <dt>

[**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ et \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

