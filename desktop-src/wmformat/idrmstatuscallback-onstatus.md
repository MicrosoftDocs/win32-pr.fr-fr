---
title: Méthode IDRMStatusCallback OnStatus
description: La méthode OnStatus reçoit les messages d’état des processus DRM asynchrones.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Méthode OnStatus format Windows Media
- Méthode OnStatus format Windows Media, interface IDRMStatusCallback
- Interface IDRMStatusCallback Windows Media format, méthode OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030096"
---
# <a name="idrmstatuscallbackonstatus-method"></a>IDRMStatusCallback :: OnStatus, méthode

La méthode **OnStatus** reçoit les messages d’état des processus DRM asynchrones.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*État* \[ dans\]
</dt> <dd>

Code d’état. Les codes de message sont définis dans le type d’énumération d' **\_ État msdrm** .

</dd> <dt>

*RH* \[ dans\]
</dt> <dd>

Code de retour qui prend en charge le message d’État.

</dd> <dt>

*dwType* \[ dans\]
</dt> <dd>

Type des données vers lesquelles pointe *pValue*. Défini sur l’une des valeurs de l’énumération de [**\_ type de \_ données de l’attr DRM**](drm-attr-datatype.md) .

</dd> <dt>

*pValue* \[ dans\]
</dt> <dd>

Pointeur vers les données relatives au message d’État. Le type de données est déterminé par la valeur du paramètre *dwType* . Pour plus d’informations, consultez l’énumération de [**\_ type de \_ données de l’attr DRM**](drm-attr-datatype.md) .

</dd> <dt>

*pvContext* \[ dans\]
</dt> <dd>

Paramètre facultatif qui peut être utilisé pour identifier l’objet qui a envoyé le message. En définissant *pvContext* quand vous inscrivez ce rappel, vous pouvez utiliser le même rappel pour gérer plusieurs processus asynchrones.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**type de données de l' \_ attr DRM \_**](drm-attr-datatype.md)
</dt> <dt>

[**Interface IDRMStatusCallback**](idrmstatuscallback.md)
</dt> </dl>

 

 





