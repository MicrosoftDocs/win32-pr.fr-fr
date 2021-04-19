---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteSmallBusiness sur 1 si Microsoft Small Business Server est installé.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: Propriété MsiNTSuiteSmallBusiness
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544084"
---
# <a name="msintsuitesmallbusiness-property"></a>Propriété MsiNTSuiteSmallBusiness

Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteSmallBusiness** sur 1 si Microsoft Small Business Server est installé. Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur SMALLBUSINESS de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Dans le cas contraire, le programme d’installation ne définit pas cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
