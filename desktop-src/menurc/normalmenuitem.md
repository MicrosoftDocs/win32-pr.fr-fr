---
title: NORMALMENUITEM, structure
description: Contient des informations sur chaque élément d’une ressource de menu qui n’ouvre pas un menu ou un sous-menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menus de la structure NORMALMENUITEM et autres ressources
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f47fef5e1481d56671cd525061f1a5fcf88481213671bac45c923cfbae0ebbd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733689"
---
# <a name="normalmenuitem-structure"></a>NORMALMENUITEM, structure

Contient des informations sur chaque élément d’une ressource de menu qui n’ouvre pas un menu ou un sous-menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>Membres

<dl> <dt>

**resInfo**
</dt> <dd>

Type : **Word**

</dd> <dd>

Type d’élément de menu. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                       | Signification                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ FIN**</dt> <dt>0x80</dt> </dl>       | L’élément de menu est le dernier dans ce sous-menu ou ressource de menu ; Cet indicateur est utilisé en interne par le système.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Menu contextuel**</dt> <dt>0x01</dt> </dl> | L’élément de menu ouvre un menu ou un sous-menu. l’indicateur est utilisé en interne par le système. <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

Type : **szOrOrd**

</dd> <dd>

Chaîne Unicode terminée par le caractère null qui contient le texte de cet élément de menu. Il n’existe aucune limite fixe quant à la taille de cette chaîne.

</dd> </dl>

## <a name="remarks"></a>Remarques

Il existe une structure **NORMALMENUITEM** pour chaque élément de menu qui n’ouvre pas un menu ou un sous-menu. Indiquez le dernier élément de menu d’un menu en affectant à **resInfo** membre la valeur **MFR \_ end**.

Un séparateur de menu est un type spécial d’élément de menu qui est inactif, mais qui apparaît sous la forme d’une barre de séparation entre deux éléments de menu actifs. Indiquez un séparateur de menu en laissant le membre **menuText** vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

 





