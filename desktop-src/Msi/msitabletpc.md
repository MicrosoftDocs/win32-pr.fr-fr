---
description: Le programme d’installation définit la propriété MsiTabletPC sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP Édition Tablet PC.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propriété MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529946"
---
# <a name="msitabletpc-property"></a>Propriété MsiTabletPC

Le programme d’installation définit la propriété **MsiTabletPC** sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP Édition Tablet PC. Le programme d’installation utilise la fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec **SM \_ TABLETPC**, et la propriété reçoit la valeur différente de zéro retournée par cette fonction. Si le système actuel n’est pas Windows XP Édition Tablet PC, la fonction **GetSystemMetrics** retourne la valeur zéro et le programme d’installation ne définit pas cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
