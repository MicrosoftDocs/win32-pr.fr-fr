---
title: IMsRdpClientAdvancedSettings3 propriété ConnectionBarShowMinimizeButton
description: Spécifie s’il faut afficher le bouton réduire sur la barre de connexion.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectionBarShowMinimizeButton
- Services Bureau à distance de la propriété ConnectionBarShowMinimizeButton, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectionBarShowMinimizeButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740012"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a>IMsRdpClientAdvancedSettings3 :: ConnectionBarShowMinimizeButton, propriété

Spécifie s’il faut afficher le bouton **réduire** sur la barre de connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la **\_ valeur variant true** pour afficher le bouton **réduire** et la **\_ valeur false à false** pour désactiver l’affichage du bouton **réduire** .

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

 

 





