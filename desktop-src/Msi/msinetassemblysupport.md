---
description: La propriété MsiNetAssemblySupport indique si l’ordinateur prend en charge les assemblys Common Language Runtime.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propriété MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021319"
---
# <a name="msinetassemblysupport-property"></a>Propriété MsiNetAssemblySupport

La propriété **MsiNetAssemblySupport** indique si l’ordinateur prend en charge les assemblys Common Language Runtime. Sur les systèmes qui prennent en charge les assemblys CLR (Common Language Runtime), le programme d’installation définit la valeur de **MsiNetAssemblySupport** sur la version de fichier de Fusion.dll. Le programme d’installation ne définit pas cette propriété si le système d’exploitation ne prend pas en charge les assemblys Common Language Runtime. Lorsque plusieurs versions de Fusion.dll sont installées côte à côte sur l’ordinateur de l’utilisateur, cette propriété est définie sur la version la plus récente du fichier Fusion.dll. par exemple, si .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15) et .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) sont installés côte à côte, la propriété **MsiNetAssemblySupport** est définie sur 1.1.4322.314. Pour plus d’informations, consultez [assemblys](assemblies.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




