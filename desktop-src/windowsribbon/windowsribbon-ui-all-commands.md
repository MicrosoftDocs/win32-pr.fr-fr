---
title: UI_ALL_COMMANDS (UIRibbon. h)
description: Spécifie une constante qui identifie la collection de commandes déclarée dans le fichier de ressources de balisage.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24767f2d3839b94ee83c6a9a527b2e80dcf8c1960e877f65a0e7e96fff4e3ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705958"
---
# <a name="ui_all_commands"></a>interface utilisateur \_ toutes les \_ commandes

Spécifie une constante qui identifie la collection de commandes déclarée dans le fichier de ressources de balisage.

## <a name="remarks"></a>Remarques

**Interface utilisateur \_ Toutes les \_ commandes** sont utiles lorsqu’il est nécessaire d’accéder à des propriétés similaires dans toutes les commandes. Par exemple, **l’interface utilisateur \_ peut être \_** passée à [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) pour invalider et actualiser toutes les commandes de ruban en interrogeant l’application hôte à la recherche de nouvelles valeurs de propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et la mise à jour de la plateforme pour les applications de bureau Windows vista \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows server 2008 R2, Windows server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 \[\]<br/> |
| En-tête<br/>                   | <dl> <dt>UIRibbon. h</dt> </dl>                                             |
| MIDL<br/>                      | <dl> <dt>UIRibbon. idl</dt> </dl>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes et énumérations](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

