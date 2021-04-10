---
title: Message EM_SETTABLEPARMS (RichEdit. h)
description: Modifie les paramètres des lignes d’une table.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941959"
---
# <a name="em_settableparms-message"></a>\_Message SETTABLEPARMS em

Modifie les paramètres des lignes d’une table.

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



| Code de retour                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ ÉCHEC**</dt> </dl>        | Les modifications ne peuvent pas être effectuées. Cela peut se produire si le contrôle est un contrôle de texte brut ou une seule ligne, ou si le point d’insertion se trouve à l’intérieur d’un objet mathématique. Elle se produit également si les tables sont désactivées, ou si le message [**\_ SETEDITSTYLEEX em**](em-seteditstyleex.md) définit la valeur sa **\_ ex \_ table** . <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *WParam* ou *lParam* a la valeur null ou pointe vers une structure non valide. Le membre **cCell** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) doit être au moins égal à 1 et inférieur à 63. Le membre **cbRow** doit être égal à `sizeof(TABLEROWPARMS)` ou `sizeof(TABLEROWPARMS)   2*sizeof(long)` . La dernière valeur est la taille de la structure **TABLEROWPARMS** RichEdit 4,1. Le membre **cbCell** de **TABLEROWPARMS** doit être égal à `sizeof(TABLECELLPARMS)` . Le point d’insertion doit être au début d’une table ou à l’intérieur d’une ligne de table, et le nombre de cellules ne peut être modifié que par un seul. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La mémoire disponible est insuffisante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Notes

Ce message modifie les paramètres du nombre de lignes spécifié par le membre **cRow** de la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , si la table contient ce nombre de lignes consécutives. Si **cRow** est inférieur à 0, le message itère jusqu’à la fin de la table. Si le nombre de cellules diffère du nombre de cellules actuel par + 1 ou 1, il insère ou supprime la cellule à l’index spécifié par le membre **iCell** de **TABLEROWPARMS**. La ligne de départ du tableau est identifiée par une position de caractère. Cette position est spécifiée par les membres **cpStartRow** dont les valeurs sont supérieures ou égales à zéro. La position doit se trouver à l’intérieur de la ligne de la table, mais pas à l’intérieur d’une table imbriquée, sauf si vous souhaitez modifier les paramètres de la table s. Si le membre **cpStartRow** est 1, la position du caractère est donnée par la sélection actuelle. Pour ce faire, placez la sélection n’importe où dans la ligne de la table ou sélectionnez la ligne contenant l’extrémité active de la sélection à la fin de la ligne du tableau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTABLEPARMS em**](em-gettableparms.md)
</dt> </dl>

 

 





