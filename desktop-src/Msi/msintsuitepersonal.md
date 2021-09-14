---
description: sur Windows xp et les systèmes d’exploitation ultérieurs, le programme d’installation affecte la valeur 1 à la propriété MsiNTSuitePersonal si le système d’exploitation est Windows XP édition personnelle.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propriété MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119765"
---
# <a name="msintsuitepersonal-property"></a>Propriété MsiNTSuitePersonal

sur Windows xp et les systèmes d’exploitation ultérieurs, le programme d’installation affecte la valeur 1 à la propriété **MsiNTSuitePersonal** si le système d’exploitation est Windows XP édition personnelle. Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur personnel de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Dans le cas contraire, le programme d’installation ne définit pas cette propriété.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
