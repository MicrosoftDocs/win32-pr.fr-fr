---
description: Sur Windows XP et les systèmes d’exploitation ultérieurs, le programme d’installation définit la propriété MsiNTSuitePersonal sur 1 si le système d’exploitation est Windows XP Édition personnelle.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propriété MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540254"
---
# <a name="msintsuitepersonal-property"></a>Propriété MsiNTSuitePersonal

Sur Windows XP et les systèmes d’exploitation ultérieurs, le programme d’installation définit la propriété **MsiNTSuitePersonal** sur 1 si le système d’exploitation est Windows XP Édition personnelle. Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur personnel de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Dans le cas contraire, le programme d’installation ne définit pas cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
