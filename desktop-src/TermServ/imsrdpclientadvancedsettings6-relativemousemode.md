---
title: IMsRdpClientAdvancedSettings6 propriété RelativeMouseMode
description: Spécifie si la souris doit utiliser le mode relatif.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RelativeMouseMode
- Services Bureau à distance de la propriété RelativeMouseMode, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RelativeMouseMode
- Services Bureau à distance de la propriété RelativeMouseMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RelativeMouseMode
- Services Bureau à distance de la propriété RelativeMouseMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RelativeMouseMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511372"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a>IMsRdpClientAdvancedSettings6 :: RelativeMouseMode, propriété

Spécifie si la souris doit utiliser le mode relatif. Contient **la \_ valeur variant true** si la souris est en mode relatif ou **\_ false** si la souris est en mode absolu.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Contient la nouvelle valeur de la propriété.

## <a name="remarks"></a>Notes

Le mode de la souris indique comment le contrôle ActiveX calcule les coordonnées de la souris qu’il envoie au serveur Bureau à distance hôte de session (hôte de session Bureau à distance). Lorsque la souris est en mode relatif, le contrôle ActiveX calcule les coordonnées de la souris par rapport à la dernière position de la souris. Lorsque la souris est en mode absolu, le contrôle ActiveX calcule les coordonnées de la souris par rapport au Bureau du serveur hôte de session Bureau à distance.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista avec SP1<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





