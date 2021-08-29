---
description: Étend l’objet IShellDispatch3.
title: Objet IShellDispatch4 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 057ef4082bac8d04c006d951db7d2d251be2f8c62e88af65bc1a69678514af81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969008"
---
# <a name="ishelldispatch4-object"></a>Objet IShellDispatch4

Étend l’objet [**IShellDispatch3**](ishelldispatch3.md) . Outre les propriétés et les méthodes prises en charge par **IShellDispatch3**, **IShellDispatch4** prend en charge quatre méthodes supplémentaires.

> [!Note]  
> **IShellDispatch4** est implémenté et accessible via l’objet [**Shell**](shell.md) .

 

## <a name="members"></a>Membres

L’objet **IShellDispatch4** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **IShellDispatch4** a ces méthodes.



| Méthode                                                     | Description                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Obtient la valeur d’une stratégie Internet Explorer spécifiée.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Récupère un paramètre d’interpréteur de commandes global.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Affiche ou masque le bureau.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | affiche la boîte de dialogue **Sécurité Windows** .<br/>            |



 

## <a name="remarks"></a>Remarques

pour plus d’informations sur les services Windows, consultez la documentation sur les [services](../services/services.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 6,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objet Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
