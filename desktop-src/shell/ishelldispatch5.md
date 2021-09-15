---
description: Étend l’objet IShellDispatch4.
title: Objet IShellDispatch5 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412448"
---
# <a name="ishelldispatch5-object"></a>Objet IShellDispatch5

Étend l’objet [**IShellDispatch4**](ishelldispatch4.md) . En plus des propriétés et des méthodes prises en charge par **IShellDispatch4**, **IShellDispatch5** ajoute une méthode qui affiche les fenêtres ouvertes dans une pile 3D.

> [!Note]  
> **IShellDispatch5** est implémenté et accessible via l’objet [**Shell**](shell.md) .

 

## <a name="members"></a>Membres

L’objet **IShellDispatch5** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **IShellDispatch5** a ces méthodes.



| Méthode                                                   | Description                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**WindowSwitcher**](ishelldispatch5-windowswitcher.md) | Affiche vos fenêtres ouvertes dans une pile 3D que vous pouvez parcourir.<br/> |



 

## <a name="requirements"></a>Spécifications



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
</dt> <dt>

[**IShellDispatch4**](ishelldispatch4.md)
</dt> </dl>

 

 
