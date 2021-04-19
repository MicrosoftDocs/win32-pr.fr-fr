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
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522332"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>D2D1CreateFactory <Factory> ( \_ type de fabrique d2d1 \_ , \_ OPTIONS de fabrique d2d1 \_&, Factory \* \* ) (fonction)

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

