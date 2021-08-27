---
title: IMsTscAdvancedSettings IndexIcône, propriété
description: Spécifie l’index de l’icône dans le fichier icône actuel.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- IndexIcône, propriété Services Bureau à distance
- IndexIcône, Services Bureau à distance de la propriété, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété IndexIcône
- IndexIcône, Services Bureau à distance de la propriété, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété IndexIcône
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c1c53a073f218666ab44eb926b9a92f835078c50a88bc488cc1da4b70b056f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125459"
---
# <a name="imstscadvancedsettingsiconindex-property"></a>IMsTscAdvancedSettings :: IndexIcône, propriété

Spécifie l’index de l’icône dans le fichier icône actuel.

> [!Note]  
> cette propriété n’est pas prise en charge dans le contrôle ActiveX (MsRdp. ocx). Il est pris en charge dans la bibliothèque MsTscAx.dll incluse dans le client standard (MsTsc.exe).

 

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a>Valeur de la propriété

Index de l’icône.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ false**.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





