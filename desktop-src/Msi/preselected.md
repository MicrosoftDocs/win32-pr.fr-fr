---
description: La propriété présélectionnée indique que des fonctionnalités ont déjà été sélectionnées et que la boîte de dialogue de sélection n’a pas besoin d’être affichée. Les expressions conditionnelles qui dépendent du fait que les fonctionnalités sont déjà installées utilisent cette valeur.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propriété présélectionnée
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a85f5c3248002fec776e45e9d7ad37550d3e16d7a5d76b098948b571b8c9c546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042319"
---
# <a name="preselected-property"></a>Propriété présélectionnée

La propriété **présélectionnée** indique que des fonctionnalités ont déjà été sélectionnées et que la boîte de dialogue de sélection n’a pas besoin d’être affichée.

Les expressions conditionnelles qui dépendent du fait que les fonctionnalités sont déjà installées utilisent cette valeur. Par exemple, la propriété peut être utilisée pour supprimer les boîtes de dialogue qui impliquent des sélections de fonctionnalités pendant la reprise d’une installation interrompue.

Le programme d’installation définit la propriété **présélectionnée** sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés suivantes est spécifiée sur la ligne de commande. Si la propriété **présélectionnée** a la valeur 1, le programme d’installation n’utilise pas la [table de conditions](condition-table.md) pour évaluer la sélection des fonctionnalités. Les fonctionnalités sont installées en fonction des propriétés suivantes. Le programme d’installation évalue toujours ces propriétés dans l’ordre suivant :

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Installez**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**INSTALLÉ**](reinstall.md)
6.  [**PUBLIÉS**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




