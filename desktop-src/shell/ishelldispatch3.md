---
description: Étend l’objet IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Objet IShellDispatch3 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8f02095415ff2682e1f2a2eeb21c4afe0754b72251f6129856f1b6a415913cf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720915"
---
# <a name="ishelldispatch3-object"></a>Objet IShellDispatch3

Étend l’objet [**IShellDispatch2**](ishelldispatch2-object.md) . **IShellDispatch3** prend en charge une nouvelle méthode en plus des propriétés et des méthodes prises en charge par **IShellDispatch2**.

> [!Note]  
> **IShellDispatch3** est implémenté et accessible via l’objet [**Shell**](shell.md) .

 

## <a name="members"></a>Membres

L’objet **IShellDispatch3** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **IShellDispatch3** a ces méthodes.



| Méthode                                             | Description                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**AddToRecent**](ishelldispatch3-addtorecent.md) | Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).<br/> |



 

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
</dt> </dl>

 

 
