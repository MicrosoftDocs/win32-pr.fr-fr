---
description: sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteDataCenter sur 1 si Windows 2000 Datacenter Server est installé.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Propriété MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b42edc0a4abb544133b4b7fb176988f826c5af172cc4c0d49ca56494ed37672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082809"
---
# <a name="msintsuitedatacenter-property"></a>Propriété MsiNTSuiteDataCenter

sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteDataCenter** sur 1 si Windows 2000 Datacenter Server est installé. Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur de centre de donnes de la suite est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Dans le cas contraire, le programme d’installation ne définit pas cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
