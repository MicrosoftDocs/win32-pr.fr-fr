---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteWebServer sur 1 si le programme d’installation s’exécute sur une édition Web du serveur Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Propriété MsiNTSuiteWebServer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545438"
---
# <a name="msintsuitewebserver-property"></a>Propriété MsiNTSuiteWebServer

Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteWebServer** sur 1 si le programme d’installation s’exécute sur une édition Web du serveur Windows Server 2003. Le programme d’installation définit cette propriété sur 1 uniquement si \_ l' \_ indicateur de panneau de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Dans le cas contraire, le programme d’installation ne définit pas cette propriété.

## <a name="remarks"></a>Notes

Cette propriété est disponible uniquement avec la version Windows Server 2003 du programme d’installation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
