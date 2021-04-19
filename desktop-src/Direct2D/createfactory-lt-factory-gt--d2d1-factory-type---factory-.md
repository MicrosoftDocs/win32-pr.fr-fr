---
title: Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
description: Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D. | Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Fonction de fabrique D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535785"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><Factory>Fonction D2D1CreateFactory ( \_ \_ type de fabrique d2d1, Factory \* \* )

Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Paramètres de modèle



| Paramètre | Description                                                 |
|-----------|-------------------------------------------------------------|
| *Fabrique* | Type de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) à créer. |



 

## <a name="parameters"></a>Paramètres



| Paramètre     | Description                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | Le modèle de thread de la fabrique et les ressources qu’il crée.                |
| *usine*     | Lorsque cette méthode est retournée, contient l’adresse d’un pointeur vers la nouvelle fabrique. |



 

## <a name="return-value"></a>Valeur renvoyée

Si la méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="examples"></a>Exemples

L’exemple suivant crée une fabrique.


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Bibliothèque<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

