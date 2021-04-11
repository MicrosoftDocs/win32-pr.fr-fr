---
description: 'La méthode IWiaItem2 :: EnumRegisterEventInfo crée un énumérateur que vous pouvez utiliser pour obtenir des informations sur les événements pour lesquels une application est inscrite.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2 :: EnumRegisterEventInfo, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113311"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>IWiaItem2 :: EnumRegisterEventInfo, méthode

La méthode **IWiaItem2 :: EnumRegisterEventInfo** crée un énumérateur que vous pouvez utiliser pour obtenir des informations sur les événements pour lesquels une application est inscrite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Non utilisé. Définit la valeur 0.

</dd> <dt>

*pEventGUID* \[ dans\]
</dt> <dd>

Type : * #*const \* GUID* _

Pointeur vers un identificateur qui spécifie l’événement matériel pour lequel vous souhaitez obtenir des informations d’inscription.

</dd> <dt>

_ppIEnum * \[ out\]
</dt> <dd>

Type : **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Adresse d’un pointeur vers l’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Une application appelle cette méthode pour créer un objet énumérateur pour les informations d’événement. **IWiaItem2 :: EnumRegisterEventInfo** stocke l’adresse de l’interface de [**\_ développement \_ IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) de l’objet énumérateur dans le paramètre *ppIEnum* . Le programme utilise ensuite le pointeur d’interface pour énumérer les propriétés de l’événement pour lequel il est enregistré.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnum* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
