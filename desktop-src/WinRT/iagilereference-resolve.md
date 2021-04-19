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
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544662"
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



 

## <a name="remarks"></a>Notes

Appelez la fonction [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) pour créer une référence agile à un objet. Appelez la méthode **Resolve** pour localiser l’objet dans le cloisonnement dans lequel **Resolve** est appelé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>            |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




