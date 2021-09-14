---
description: le programme d’installation définit la propriété MsiNTProductType pour les systèmes d’exploitation Windows NT, Windows 2000 et versions ultérieures.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propriété MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021315"
---
# <a name="msintproducttype-property"></a>Propriété MsiNTProductType

le programme d’installation définit la propriété **MsiNTProductType** pour les systèmes d’exploitation Windows NT, Windows 2000 et versions ultérieures. cette propriété indique le type de produit Windows.

pour les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit les valeurs suivantes. Notez que les valeurs sont les mêmes que celles du champ **wProductType** de la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .



| Valeur | Signification                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional et versions ultérieures      |
| 2     | Windows contrôleur de domaine 2000 et versions ultérieures |
| 3     | Windows serveur 2000 et versions ultérieures            |



 

pour les systèmes d’exploitation antérieurs à Windows 2000, le programme d’installation définit les valeurs suivantes.



| Valeur | Signification                      |
|-------|------------------------------|
| 1     | Windows Station de travail NT       |
| 2     | Windows Contrôleur de domaine NT |
| 3     | Windows Serveur NT            |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 
