---
description: Le programme d’installation définit la propriété MsiNTProductType pour les systèmes d’exploitation Windows NT, Windows 2000 et versions ultérieures.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propriété MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537568"
---
# <a name="msintproducttype-property"></a>Propriété MsiNTProductType

Le programme d’installation définit la propriété **MsiNTProductType** pour les systèmes d’exploitation Windows NT, Windows 2000 et versions ultérieures. Cette propriété indique le type de produit Windows.

Pour les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit les valeurs suivantes. Notez que les valeurs sont les mêmes que celles du champ **wProductType** de la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .



| Valeur | Signification                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 professionnel et versions ultérieures      |
| 2     | Contrôleur de domaine Windows 2000 et versions ultérieures |
| 3     | Windows 2000 Server et versions ultérieures            |



 

Pour les systèmes d’exploitation antérieurs à Windows 2000, le programme d’installation définit les valeurs suivantes.



| Valeur | Signification                      |
|-------|------------------------------|
| 1     | Station de travail Windows NT       |
| 2     | Contrôleur de domaine Windows NT |
| 3     | Windows NT Server            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
