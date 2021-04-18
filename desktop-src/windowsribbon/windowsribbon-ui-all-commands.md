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
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511936"
---
# <a name="ui_all_commands"></a>interface utilisateur \_ toutes les \_ commandes

Spécifie une constante qui identifie la collection de commandes déclarée dans le fichier de ressources de balisage.

## <a name="remarks"></a>Notes

**Interface utilisateur \_ Toutes les \_ commandes** sont utiles lorsqu’il est nécessaire d’accéder à des propriétés similaires dans toutes les commandes. Par exemple, **l’interface utilisateur \_ peut être \_** passée à [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) pour invalider et actualiser toutes les commandes de ruban en interrogeant l’application hôte à la recherche de nouvelles valeurs de propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de plateforme pour les applications de bureau Windows Server 2008 \[ uniquement\]<br/> |
| En-tête<br/>                   | <dl> <dt>UIRibbon. h</dt> </dl>                                             |
| MIDL<br/>                      | <dl> <dt>UIRibbon. idl</dt> </dl>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes et énumérations](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

