---
description: La méthode GetAt récupère un élément de la collection à l’aide d’un index de base zéro.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'IPortableDeviceValuesCollection :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542437"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection :: GetAt, méthode

La méthode **GetAt** récupère un élément de la collection à l’aide d’un index de base zéro.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

**Valeur DWORD** qui spécifie un index de base zéro dans la collection.

</dd> <dt>

*ppValues* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) à partir de la collection. L’appelant est responsable de l’appel de **Release** sur cette interface lorsqu’il est terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | S_OK<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’index de base zéro qui a été passé était hors limites.<br/>             |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Un argument de pointeur obligatoire était **null**.<br/>                             |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | La collection contient un pointeur **IPortableDeviceValues** **null** .<br/> |



 

## <a name="remarks"></a>Notes

Toutes les modifications apportées aux valeurs dans l’interface récupérée seront apportées à la version stockée dans la collection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




