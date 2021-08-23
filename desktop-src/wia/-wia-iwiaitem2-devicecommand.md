---
description: envoie une commande à un périphérique matériel WIA (Windows Image Acquisition) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2 ::D méthode eviceCommand (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f70fd7b4a987dac3a079651f2cbc04dc50817ba8a43f8da1449a3f605683ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706309"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2 ::D méthode eviceCommand

envoie une commande à un périphérique matériel WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*pCmdGUID* \[ dans\]
</dt> <dd>

Type : **const GUID \***

Spécifie la commande à envoyer à l’appareil WIA 2,0. Consultez [**commandes de l’appareil WIA**](-wia-wia-device-commands.md).

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’élément [**IWiaItem2**](-wia-iwiaitem2.md) créé par la commande, le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

En plus des codes d’erreur COM standard, la méthode peut retourner la valeur suivante.



| Code de retour                                                                                       | Description                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_CMDNOTSUPPORTED E**</dt> </dl> | La commande n’est pas implémentée pour l’interface [**IWiaItem2**](-wia-iwiaitem2.md) sur laquelle la méthode est appelée. La valeur numérique de cette erreur n’est pas encore définie. <br/> |



 

## <a name="remarks"></a>Remarques

Le comportement de cette méthode est différent selon la catégorie du nœud sur lequel la méthode est appelée.

Lorsque l’application envoie la commande [**WIA \_ cmd \_ Take \_ image**](-wia-wia-device-commands.md) à l’appareil à l’aide de la méthode **IWiaItem2 ::D EVICECOMMAND** , le système d’exécution WIA 2,0 crée un objet [**IWiaItem2**](-wia-iwiaitem2.md) pour représenter l’image. La méthode **IWiaItem2 ::D evicecommand** stocke l’adresse de l’interface dans le paramètre *ppIWiaItem2* .

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
