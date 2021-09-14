---
description: La propriété date est le mois, le jour et l’année en cours sous la forme d’une chaîne de texte littéral au format MM/jj/aaaa.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091666"
---
# <a name="date-property"></a>Date, propriété

La propriété **Date** est le mois, le jour et l’année en cours sous la forme d’une chaîne de texte littéral au format mm/jj/aaaa. Par exemple, la date du 22 juin 2005 peut être représentée sous la forme « 06/22/2005 ». Le format de la valeur dépend des paramètres régionaux de l’utilisateur, et est le format obtenu à l’aide de [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) avec l' \_ option Date SHORTDATE. la valeur de cette propriété est définie par le Windows Installer et non par l’auteur du package.

## <a name="remarks"></a>Notes

Comme il s’agit d’une chaîne de texte, elle ne peut pas être utilisée dans les expressions conditionnelles.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

