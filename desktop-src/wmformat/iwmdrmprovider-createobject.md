---
title: IWMDRMProvider CreateObject, méthode (wmdrmsdk. h)
description: La méthode CreateObject récupère un pointeur vers une interface spécifiée, en créant l’objet d’implémentation, si nécessaire.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Méthode CreateObject Windows Media format
- Méthode CreateObject Windows Media format, interface IWMDRMProvider
- Interface IWMDRMProvider Windows Media format, CreateObject, méthode
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50341e33092b33b19ec3f41d968e0a1b7bc883ae959b200f6c7062e4c69996b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700775"
---
# <a name="iwmdrmprovidercreateobject-method"></a>IWMDRMProvider :: CreateObject, méthode

La méthode **CreateObject** récupère un pointeur vers une interface spécifiée, en créant l’objet d’implémentation, si nécessaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* \[ dans\]
</dt> <dd>

Identificateur de l’interface à créer. Définissez l’une des valeurs suivantes.

-   IID \_ IWMDRMLicenseManagement
-   IID \_ IWMDRMLicenseQuery
-   IID \_ IWMDRMNetReceiver
-   IID \_ IWMDRMNetTransmitter
-   IID \_ IWMDRMSecurity

</dd> <dt>

*ppvObject* \[ à\]
</dt> <dd>

Adresse d’un pointeur qui reçoit l’adresse de l’interface demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMProvider**](iwmdrmprovider.md)
</dt> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





