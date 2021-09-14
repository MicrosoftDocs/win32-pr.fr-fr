---
title: ExStyle (instruction)
description: Définit des styles de fenêtre étendus pour une boîte de dialogue. Dans une définition de ressource, l’instruction ExStyle est placée avec les instructions facultatives avant le début du corps de la définition de ressource.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menus d’instruction ExStyle et autres ressources
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220780"
---
# <a name="exstyle-statement"></a>ExStyle (instruction)

Définit des styles de fenêtre étendus pour une boîte de dialogue. Dans une définition de ressource, l’instruction **ExStyle** est placée avec les instructions facultatives avant le début du corps de la définition de ressource.

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*style étendu*
</dt> <dd>

Style de fenêtre étendu pour la boîte de dialogue ou le contrôle. Pour obtenir la liste des styles de fenêtre étendus, consultez [**styles de fenêtre étendus**](/windows/desktop/winmsg/extended-window-styles).

</dd> </dl>

## <a name="remarks"></a>Notes

Pour les contrôles, les styles étendus sont spécifiés après l’option *style* dans l’instruction Control Resource-Definition. Pour plus d’informations, consultez l’instruction de définition de ressource pour le contrôle individuel.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**RÉGULATION**](control-control.md)
</dt> <dt>

[**DIALOGUE**](dialog-resource.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**MESSAGES**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[Ressource définie par l’utilisateur](user-defined-resource.md)
</dt> </dl>

 

 