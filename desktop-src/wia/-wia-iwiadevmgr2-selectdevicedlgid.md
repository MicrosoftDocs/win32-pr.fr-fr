---
description: Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2 :: SelectDeviceDlgID, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517549"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>IWiaDevMgr2 :: SelectDeviceDlgID, méthode

Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
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

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Type : **BSTR \** _

Pointeur vers une chaîne qui reçoit la chaîne d’identificateur de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                                  | Description                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | L’appareil a été sélectionné avec succès. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | L’utilisateur a annulé la boîte de dialogue. <br/>                                                              |
| <dl> <dt>**WIA \_ - \_ aucun \_ appareil \_ disponible**</dt> </dl> | Aucun périphérique matériel WIA 2,0 ne correspond aux spécifications indiquées dans le paramètre *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Notes

Cette méthode crée et affiche la boîte de dialogue **Sélectionner un appareil** afin que l’utilisateur puisse sélectionner un appareil WIA 2,0 pour l’acquisition d’images. Si un appareil est sélectionné avec succès, la méthode **IWiaDevMgr2 :: SelectDeviceDlgID** passe sa chaîne d’identificateur à l’application par le biais de son paramètre *pbstrDeviceID* .

L’application peut limiter les appareils affichés à l’utilisateur à des types particuliers en spécifiant les types d’appareils via le paramètre *lDeviceType* . Si un seul périphérique répond à la spécification, **IWiaDevMgr2 :: SelectDeviceDlgID** n’affiche pas la boîte de dialogue **Sélectionner un périphérique** . Au lieu de cela, il transmet la chaîne d’identificateur de l’appareil à l’application sans afficher la boîte de dialogue. Vous pouvez remplacer ce comportement et forcer **IWiaDevMgr2 :: SelectDeviceDlgID** à afficher la boîte de dialogue en passant WIA \_ Select \_ Device \_ NODEFAULT comme valeur du paramètre *lFlags* . Si plus d’un appareil WIA 2,0 correspond à la spécification, tous les appareils correspondants sont affichés dans la boîte de dialogue SelectDevice pour que l’utilisateur puisse en choisir un.

> [!Note]  
> Il est recommandé que les applications rendent la sélection de l’appareil et de l’image disponible via un élément de menu nommé **à partir de scanner** dans le menu **fichier** .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




