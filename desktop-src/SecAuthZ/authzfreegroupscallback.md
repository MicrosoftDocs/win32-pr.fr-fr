---
description: Fonction définie par l’application qui libère de la mémoire allouée par la fonction AuthzComputeGroupsCallback. AuthzFreeGroupsCallback est un espace réservé pour le nom de la fonction définie par l’application.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: AuthzFreeGroupsCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760827"
---
# <a name="authzfreegroupscallback-callback-function"></a>AuthzFreeGroupsCallback fonction de rappel

La fonction **AuthzFreeGroupsCallback** est une fonction définie par l’application qui libère de la mémoire allouée par la fonction [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) . **AuthzFreeGroupsCallback** est un espace réservé pour le nom de la fonction définie par l’application.

## <a name="syntax"></a>Syntaxe


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSidAttrArray* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire allouée par [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction de rappel ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.

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

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




