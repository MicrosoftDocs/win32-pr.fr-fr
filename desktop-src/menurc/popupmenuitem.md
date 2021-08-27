---
title: POPUPMENUITEM, structure
description: Contient des informations sur les éléments de menu d’une ressource de menu qui ouvrent un menu ou un sous-menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menus de la structure POPUPMENUITEM et autres ressources
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62d769e9756f0d15e7377a79f9aa94802a469746807e3a32b5ba329f76484b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011699"
---
# <a name="popupmenuitem-structure"></a>POPUPMENUITEM, structure

Contient des informations sur les éléments de menu d’une ressource de menu qui ouvrent un menu ou un sous-menu. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a>Membres

<dl> <dt>

**type**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Décrit l’élément de menu. Parmi les valeurs que ce membre peut avoir, citons celles répertoriées dans la liste ci-dessous.

Outre les valeurs affichées, ce membre peut également être une combinaison des valeurs de type répertoriées avec le membre **ftype** de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Les valeurs de type sont celles qui commencent par MFT \_ . Pour utiliser ces valeurs de type MFT prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :

`#include "winuser.h"`



| Valeur                                                                                                                                                                                                    | Signification                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ FIN**</dt> <dt>0x80</dt> </dl>       | L’élément de menu est le dernier dans le menu ; l’indicateur est utilisé en interne par le système. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ Menu contextuel**</dt> <dt>0x01</dt> </dl> | L’élément de menu ouvre un menu ou un sous-menu. l’indicateur est utilisé en interne par le système. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Décrit l’élément de menu. Ce membre peut être une combinaison des valeurs d’État figurant dans le membre **dwState** de la structure [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Les valeurs d’État sont celles qui commencent par MFS \_ . Pour utiliser ces valeurs d’État MFS prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Expression numérique qui identifie l’élément de menu qui est passé dans le message de [**\_ commande WM**](wm-command.md) .

</dd> <dt>

**resInfo**
</dt> <dd>

Type : **Word**

</dd> <dd>

Jeu d’indicateurs binaires qui spécifient le type d’élément de menu. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                       | Signification                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ FIN**</dt> <dt>0x80</dt> </dl>       | L’élément de menu est le dernier dans ce sous-menu ou ressource de menu ; Cet indicateur est utilisé en interne par le système.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ Menu contextuel**</dt> <dt>0x01</dt> </dl> | L’élément de menu ouvre un menu ou un sous-menu. l’indicateur est utilisé en interne par le système.<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Type : **szOrOrd**

</dd> <dd>

Chaîne Unicode terminée par le caractère null qui contient le texte de cet élément de menu. Il n’existe aucune limite fixe quant à la taille de cette chaîne.

</dd> </dl>

## <a name="remarks"></a>Remarques

Il existe une structure **POPUPMENUITEM** pour chaque élément de menu qui ouvre un menu ou un sous-menu. Identifiez ce type d’élément de menu en définissant le paramètre membre de **type** sur la **\_ fenêtre contextuelle MF** et en définissant le bit **MFR \_ Popup** dans le membre **resInfo** sur 0x0001. Dans ce cas, les données finales écrites dans la ressource de [**\_ menu RT**](/windows/desktop/menurc/resource-types) du menu ou du sous-menu sont la structure [**MENUHELPID**](menuhelpid.md) . **MENUHELPID** contient une expression numérique qui identifie le menu lors du traitement de [**\_ l’aide WM**](../shell/wm-help.md) .

En outre, chaque structure **POPUPMENUITEM** qui a le **bit MFR \_ Popup** défini dans le membre **ResInfo** sera suivie d’une structure [**MENUHELPID**](menuhelpid.md) plus un nombre supplémentaire de structures **POPUPMENUITEM** , une pour chaque élément de menu dans ce sous-menu. La dernière structure **POPUPMENUITEM** dans le sous-menu aura le bit de **\_ fin MFR** défini dans le membre **resInfo** . Pour trouver la fin de la ressource, recherchez une **\_ terminaison MFR** correspondante pour chaque **\_ Popup MFR** plus une **\_ terminaison MFR** supplémentaire qui correspond au jeu d’éléments de menu le plus à l’extérieur.

Indiquez le dernier élément de menu en affectant à membre de **type** la valeur **\_ fin MF**. Étant donné que vous pouvez imbriquer des sous-menus, il peut y avoir plusieurs niveaux de **\_ terminaison MF**. Dans ces cas, les éléments de menu sont séquentiels.

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

[**MENUHELPID**](menuhelpid.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

