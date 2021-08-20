---
description: 'La propriété Time est l’heure actuelle en heures, minutes et secondes sous la forme d’une chaîne de texte littéral au format HH : MM : SS avec une horloge de 24 heures.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propriété Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050d6897b966017a18241ed7e0374174e5343f48f16e311923b1c7564f012681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141791"
---
# <a name="time-property"></a>Propriété Time

La propriété **Time** est l’heure actuelle en heures, minutes et secondes sous la forme d’une chaîne de texte littéral au format hh : mm : SS avec une horloge de 24 heures. Par exemple, l’heure 6:57 p.m. est représenté par « 18:57:00 ». Le format de la valeur dépend des paramètres régionaux de l’utilisateur, et est le format obtenu à l’aide de la fonction [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) avec l' \_ option Time FORCE24HOURFORMAT \| Time \_ NOTIMEMARKER. la valeur de cette propriété est définie par le Windows Installer et non par l’auteur du package.

## <a name="remarks"></a>Remarques

Comme il s’agit d’une chaîne de texte, elle ne peut pas être utilisée dans les expressions conditionnelles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
