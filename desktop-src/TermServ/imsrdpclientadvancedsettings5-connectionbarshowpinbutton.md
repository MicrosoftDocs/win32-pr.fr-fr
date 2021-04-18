---
title: IMsRdpClientAdvancedSettings5 propriété ConnectionBarShowPinButton
description: Définit ou récupère la configuration du bouton épingler dans la barre de connexion.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectionBarShowPinButton
- Services Bureau à distance de la propriété ConnectionBarShowPinButton, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectionBarShowPinButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512561"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a>IMsRdpClientAdvancedSettings5 :: ConnectionBarShowPinButton, propriété

Définit ou récupère la configuration du bouton épingler dans la barre de connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne **true** ou **false**. La valeur **true** affiche le bouton épingler dans la barre de connexion. La valeur **false** masque le bouton épingler dans la barre de connexion.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





