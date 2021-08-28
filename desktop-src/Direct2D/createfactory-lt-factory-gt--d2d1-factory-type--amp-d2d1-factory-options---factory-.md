---
title: Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D. | Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) fonction Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08562269bc682b9138f2413c33b41ad3d2aebf7d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885086"
---
# <a name="d2d1createfactoryltfactorygtd2d1_factory_typed2d1_factory_optionsfactory-function"></a>&lt;Fabrique D2D1CreateFactory &gt; ( \_ type de fabrique d2d1 \_ , \_ options de fabrique d2d1 \_&, fabrique \* \* ) (fonction)

Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Paramètres de modèle



| Paramètre | Description                                                 |
|-----------|-------------------------------------------------------------|
| *Fabrique* | Type de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) à créer. |



 

## <a name="parameters"></a>Paramètres



| Paramètre        | Description                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | Le modèle de thread de la fabrique et les ressources qu’il crée.                |
| *factoryOptions* | Niveau de détail fourni à la couche de débogage.                            |
| *usine*        | Lorsque cette méthode est retournée, contient l’adresse d’un pointeur vers la nouvelle fabrique. |



 

## <a name="return-value"></a>Valeur renvoyée

Si la méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ desktop apps \|\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[ desktop apps \|\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

