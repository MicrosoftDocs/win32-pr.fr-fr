---
title: Message LVM_SORTITEMSEX (commctrl. h)
description: Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View. L’index de chaque élément change pour refléter la nouvelle séquence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SortItemsEx.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032427"
---
# <a name="lvm_sortitemsex-message"></a>\_Message SORTITEMSEX LVM

Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View. L’index de chaque élément change pour refléter la nouvelle séquence. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur définie par l’application qui est passée à la fonction de comparaison.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une fonction de comparaison définie par l’application. Elle est appelée au cours de l’opération de tri chaque fois que l’ordre relatif de deux éléments de liste doit être comparé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La fonction de comparaison se présente sous la forme suivante :

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Ce message est similaire à [**LVM \_ SORTITEMS**](lvm-sortitems.md), à l’exception du type d’informations passé à la fonction de comparaison. Avec **LVM \_ SORTITEMSEX**, *lParam1* est l’index actuel du premier élément, et *lParam2* est l’index actuel du deuxième élément. Vous pouvez envoyer un [**message \_ GETITEMTEXT LVM**](lvm-getitemtext.md) pour récupérer plus d’informations sur un élément, si nécessaire.

La fonction de comparaison doit retourner une valeur négative si le premier élément doit précéder le deuxième, une valeur positive si le premier élément doit suivre le deuxième, ou zéro si les deux éléments sont équivalents.

> [!Note]  
> Durant le processus de tri, le contenu de l’affichage de liste est instable. Si la fonction de rappel envoie des messages au contrôle List-View à part de [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), les résultats sont imprévisibles.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





