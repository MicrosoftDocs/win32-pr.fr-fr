---
title: WMDRMCreateProvider, fonction (wmdrmsdk. h)
description: la fonction WMDRMCreateProvider crée une fabrique de classes qui peut créer les autres objets du Windows les api étendues du Client DRM Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- WMDRMCreateProvider fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82de65423d5bc6ad2fbd55e3d8e4c97e8f63f6f7d6b6203e092176a4afc0183c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006559"
---
# <a name="wmdrmcreateprovider-function"></a>WMDRMCreateProvider fonction)

la fonction **WMDRMCreateProvider** crée une fabrique de classes qui peut créer les autres objets du Windows les api étendues du Client DRM Media. Cette fonction ne nécessite pas de bibliothèque de stubs de la part de Microsoft et crée des objets qui ne prennent pas en charge les fonctionnalités DRM protégées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDRMProvider* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IWMDRMProvider**](iwmdrmprovider.md) de l’objet nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





