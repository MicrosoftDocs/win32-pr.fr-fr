---
description: le programme d’installation définit la propriété MsiTabletPC sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP édition Tablet PC.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propriété MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac47dd0d8db3c0e882a965685bb1507dc0103f3e965dfbcb8f4857ada19e17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145608"
---
# <a name="msitabletpc-property"></a>Propriété MsiTabletPC

le programme d’installation définit la propriété **MsiTabletPC** sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP édition Tablet PC. Le programme d’installation utilise la fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec **SM \_ TABLETPC**, et la propriété reçoit la valeur différente de zéro retournée par cette fonction. si le système actuel n’est pas Windows XP édition Tablet PC, la fonction **GetSystemMetrics** retourne la valeur zéro et le programme d’installation ne définit pas cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
