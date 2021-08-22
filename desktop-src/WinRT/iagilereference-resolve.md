---
description: Obtient l’ID d’interface d’une référence agile à un objet.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'IAgileReference :: Resolve, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 0b58013ba81bb394715a0042f3f3d7435a381fa01f5b985bd9ad81d12122441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758773"
---
# <a name="iagilereferenceresolve-method"></a>IAgileReference :: Resolve, méthode

Obtient l’ID d’interface d’une référence agile à un objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* \[ dans\]
</dt> <dd>

ID d’interface de l’interface à récupérer à partir de la référence agile. Il n’est pas nécessaire qu’il soit identique à l’interface inscrite.

</dd> <dt>

*ppvObjectReference* \[ out, retval\]
</dt> <dd>

Une fois l’opération terminée, \* *ppvObjectReference* est un pointeur vers l’interface spécifiée par *riid*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur retournée                                                                              | Description                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>\_OK</dt> </dl>          | La commande s'est correctement terminée.<br/>                                  |
| <dl> <dt>E \_ NOinterface</dt> </dl> | L’interface demandée n’est pas implémentée sur l’objet inscrit.<br/> |



 

## <a name="remarks"></a>Remarques

Appelez la fonction [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) pour créer une référence agile à un objet. Appelez la méthode **Resolve** pour localiser l’objet dans le cloisonnement dans lequel **Resolve** est appelé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




