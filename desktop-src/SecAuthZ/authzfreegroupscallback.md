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
ms.openlocfilehash: 3cce78e261892fede79fb8fc76bc5b0d009342db3e0bf672be2854cb8492bcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783763"
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

## <a name="remarks"></a>Remarques

Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                   |
| Composant redistribuable<br/>          | Windows Pack des outils d’Administration du serveur 2003 sur Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de base Access Control](authorization-functions.md)
</dt> <dt>

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




