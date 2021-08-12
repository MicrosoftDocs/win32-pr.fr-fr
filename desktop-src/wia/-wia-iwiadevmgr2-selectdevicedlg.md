---
description: 'IWiaDevMgr2 :: SelectDeviceDlg, méthode-affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2 :: SelectDeviceDlg, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 344b13ec05e6f1d06011b3555e5b455202e5848b5000e799540d9f7c3160653b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441234"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>IWiaDevMgr2 :: SelectDeviceDlg, méthode

Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Spécifie la fenêtre parente de la boîte de dialogue **Sélectionner un périphérique** .

</dd> <dt>

*lDeviceType* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie le type d’appareil WIA 2,0 à utiliser. Pour obtenir la liste des valeurs possibles, consultez [spécificateurs de type d’appareil WIA](-wia-wia-device-type-specifiers.md) .

</dd> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie le comportement de la boîte de dialogue. La valeur peut être l’une des suivantes.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Utiliser le comportement par défaut.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA- \_ Sélectionner un \_ appareil \_ par défaut**


</dt> <dd>

Affiche la boîte de dialogue même s’il n’y a qu’un seul appareil correspondant.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ in, out\]
</dt> <dd>

Type : **BSTR \***

Lors de la sortie, reçoit une chaîne qui contient la chaîne d’identificateur de l’appareil. En entrée, transmettez l’adresse d’un pointeur si ces informations sont nécessaires, ou la **valeur null** si elle n’est pas nécessaire.

</dd> <dt>

*ppItemRoot* \[ out, retval\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément racine de l’arborescence hiérarchique qui représente l’appareil WIA 2,0 sélectionné. Si aucun appareil n’est trouvé, la **valeur null** est reçue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                                  | Description                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | L’appareil a été sélectionné avec succès. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | L’utilisateur a annulé la boîte de dialogue. <br/>                                                              |
| <dl> <dt>**WIA \_ - \_ aucun \_ appareil \_ disponible**</dt> </dl> | Aucun périphérique matériel WIA 2,0 ne correspond aux spécifications indiquées dans le paramètre *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode crée et affiche la boîte de dialogue **Sélectionner un appareil** afin que l’utilisateur puisse sélectionner un appareil WIA 2,0 pour l’acquisition d’images. Si un appareil est sélectionné avec succès, la méthode **IWiaDevMgr2 :: SelectDeviceDlg** crée une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) pour l’appareil. Elle stocke un pointeur vers l’interface **IWiaItem2** de l’élément racine dans le paramètre *ppItemRoot*.

L’application peut limiter les appareils affichés à l’utilisateur à des types particuliers en spécifiant les types d’appareils via le paramètre *lDeviceType* . Si un seul périphérique répond à la spécification, **IWiaDevMgr2 :: SelectDeviceDlg** n’affiche pas la boîte de dialogue **Sélectionner un périphérique** . Au lieu de cela, il crée l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) pour l’appareil et stocke un pointeur vers l’interface **IWiaItem2** de l’élément racine dans le paramètre *ppItemRoot*. Vous pouvez remplacer ce comportement et forcer **IWiaDevMgr2 :: SelectDeviceDlg** à afficher la boîte de dialogue en spécifiant \_ WIA \_ Select \_ Device NODEFAULT comme valeur du paramètre *lFlags* . Si plus d’un appareil WIA 2,0 correspond à la spécification, tous les appareils correspondants s’affichent dans la boîte de dialogue **Sélectionner un périphérique** afin que l’utilisateur puisse en choisir un.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppItemRoot* .

> [!Note]  
> Il est recommandé que les applications rendent la sélection de l’appareil et de l’image disponible via un élément de menu nommé **à partir de scanner** dans le menu **fichier** .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
