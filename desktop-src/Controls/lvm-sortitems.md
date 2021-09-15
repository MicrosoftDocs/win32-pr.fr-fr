---
title: Message LVM_SORTITEMS (commctrl. h)
description: Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View. L’index de chaque élément change pour refléter la nouvelle séquence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SortItems.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312609"
---
# <a name="lvm_sortitems-message"></a>\_Message SORTITEMS LVM

Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View. L’index de chaque élément change pour refléter la nouvelle séquence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur définie par l’application qui est passée à la fonction de comparaison.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la fonction de comparaison définie par l’application. La fonction de comparaison est appelée au cours de l’opération de tri chaque fois que l’ordre relatif de deux éléments de liste doit être comparé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La fonction de comparaison se présente sous la forme suivante :

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

Le paramètre *lParam1* est la valeur associée au premier élément comparé, tandis que le paramètre *lParam2* est la valeur associée au deuxième élément. Il s’agit des valeurs qui ont été spécifiées dans le membre **lParam** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) des éléments quand elles ont été insérées dans la liste. Le paramètre *wParam* de [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)est passé à la fonction de rappel comme troisième paramètre.

La fonction de comparaison doit retourner une valeur négative si le premier élément doit précéder le deuxième, une valeur positive si le premier élément doit suivre le deuxième, ou zéro si les deux éléments sont équivalents.

> [!Note]  
> Durant le processus de tri, le contenu de l’affichage de liste est instable. Si la fonction de rappel envoie des messages au contrôle List-View à part de [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), les résultats sont imprévisibles.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





