---
title: Méthode INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: Est utilisé par l’algorithme SHA pour comparer les demandes SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Méthode CompareSoHRequests NAP
- Méthode CompareSoHRequests NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011645"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>INapSystemHealthAgentCallback :: CompareSoHRequests, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentCallback :: CompareSoHRequests** est utilisée par l’algorithme SHA pour comparer les demandes SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LHS* \[ dans\]
</dt> <dd>

Pointeur vers le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à gauche de l’opération de comparaison.

</dd> <dt>

*RHS* \[ dans\]
</dt> <dd>

Pointeur vers le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à droite de l’opération de comparaison.

</dd> <dt>

*IsEqual* \[ à\]
</dt> <dd>

Pointeur vers un **booléen** qui a la **valeur true** si *LHS* et *RHS* sont sémantiquement égaux, et **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                               | Description                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Indique la réussite de l’opération.<br/>                         |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | La méthode n’a pas été implémentée par l’algorithme SHA.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.

L’algorithme SHA doit comparer le SoHs et retourner la **valeur true** si les SoHs sont sémantiquement égaux. Le NapAgent utilise ces informations pour déterminer si un échange SoH doit être initié en raison de la modification de l’état de l’ordinateur client.

Si les Sha ont placé des ID incrémentiels ou des horodateurs dans leur SoH, les SoHs peuvent être sémantiquement égaux (c’est-à-dire qu’ils peuvent communiquer les mêmes informations d’intégrité), mais ils peuvent être inégaux en octets. L’SHA doit implémenter cette fonction pour vérifier l’égalité sémantique de SoHs.

Si les utilisateurs de l’intégrité du système n’ont pas placé de datage ou d’ID dans leur SoHs, ils peuvent choisir de ne pas implémenter cette fonction et de retourner **E \_ NOTIMPL**. Dans ce cas, le NapAgent effectue une comparaison au niveau des octets sur [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**Intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





