---
title: IMsRdpClientAdvancedSettings3 propriété ConnectionBarShowRestoreButton
description: Spécifie s’il faut afficher le bouton restaurer sur la barre de connexion.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectionBarShowRestoreButton
- Services Bureau à distance de la propriété ConnectionBarShowRestoreButton, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectionBarShowRestoreButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384039"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a>IMsRdpClientAdvancedSettings3 :: ConnectionBarShowRestoreButton, propriété

Spécifie s’il faut afficher le bouton **restaurer** sur la barre de connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez la valeur **Variant \_ true** pour afficher le bouton **restaurer** et la valeur false à la valeur **\_ false** pour désactiver l’affichage du bouton **restaurer** .

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Cette propriété ne peut pas être définie lorsque le contrôle est connecté.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 est défini en tant que 19cd856b-c542-4c53-acee-f127e3be1a59<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





