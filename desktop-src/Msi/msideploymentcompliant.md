---
description: la propriété MSIDEPLOYMENTCOMPLIANT peut être définie pour indiquer au programme d’installation que le package a été créé et testé pour se conformer au contrôle de compte d’utilisateur (UAC) dans Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Propriété MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011879"
---
# <a name="msideploymentcompliant-property"></a>Propriété MSIDEPLOYMENTCOMPLIANT

la propriété **MSIDEPLOYMENTCOMPLIANT** peut être définie pour indiquer au programme d’installation que le package a été créé et testé pour se conformer au [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) dans Windows Vista. si cette propriété n’est pas définie, le programme d’installation détermine si le package est conforme au contrôle de compte d’utilisateur sur Windows Vista.

pour plus d’informations sur le contrôle de compte d’utilisateur et la Windows Installer, consultez [utilisation de Windows Installer avec uac](using-windows-installer-with-uac.md) et [instructions pour les Packages](guidelines-for-packages.md).

**Windows Installer 3,1, Windows Installer 3,0 et Windows Installer 2,0 :** Cette propriété est ignorée. cette propriété est utilisée uniquement par Windows Installer 4,0 dans Windows Vista.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




