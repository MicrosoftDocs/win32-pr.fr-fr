---
title: Message EM_GETTABLEPARMS (RichEdit. h)
description: Récupère les paramètres de table pour une ligne de table et les paramètres de cellule pour le nombre spécifié de cellules.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ddca96ce29a0f7b7076580b48cfeceecf1f638830b7c77bc9406a39e97de57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545029"
---
# <a name="em_gettableparms-message"></a>\_Message GETTABLEPARMS em

Récupère les paramètres de table pour une ligne de table et les paramètres de cellule pour le nombre spécifié de cellules.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur suivants.



| Code de retour                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ ÉCHEC**</dt> </dl>        | Les modifications ne peuvent pas être effectuées. Cela peut se produire si le contrôle est un contrôle de texte brut ou une seule ligne, ou si le point d’insertion se trouve à l’intérieur d’un objet mathématique. Elle se produit également si les tables sont désactivées si le message [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) définit la valeur sa **\_ ex \_ table** . <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* ou *lParam* a la valeur null ou pointe vers une structure non valide. Le membre **cbRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) doit être égal à `sizeof(TABLEROWPARMS)` ou sizeof (TABLEROWPARMS) 2 \* sizeof (long). La dernière valeur est la taille de la structure **TABLEROWPARMS** RichEdit 4,1. Le membre **cbCell** de la structure **TABLEROWPARMS** doit être égal à `sizeof(TABLECELLPARMS)` . La position du caractère de requête doit être au niveau d’un délimiteur de ligne de table. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La mémoire disponible est insuffisante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Remarques

Ce message obtient les paramètres de table pour la ligne à la position de caractère spécifiée par le membre **cpStartRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , ainsi que le nombre de cellules spécifié par le membre **cCells** de la structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

La position du caractère spécifiée par le membre **cpStartRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) doit se trouver au début de la ligne de la table ou au délimiteur de fin de la ligne de la table. Si **cpStartRow** a la valeur 1, la position du caractère est donnée par la sélection actuelle. Dans ce cas, positionnez la sélection à la fin de la ligne (entre la marque de cellule et le délimiteur de fin de la ligne de table), ou sélectionnez la ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTABLEPARMS em**](em-settableparms.md)
</dt> </dl>

 

 





