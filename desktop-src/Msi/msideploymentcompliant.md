---
description: La propriété MSIDEPLOYMENTCOMPLIANT peut être définie pour indiquer au programme d’installation que le package a été créé et testé pour se conformer au contrôle de compte d’utilisateur (UAC) dans Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Propriété MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540518"
---
# <a name="msideploymentcompliant-property"></a>Propriété MSIDEPLOYMENTCOMPLIANT

La propriété **MSIDEPLOYMENTCOMPLIANT** peut être définie pour indiquer au programme d’installation que le package a été créé et testé pour se conformer au [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) dans Windows Vista. Si cette propriété n’est pas définie, le programme d’installation détermine si le package est conforme au contrôle de compte d’utilisateur sur Windows Vista.

Pour plus d’informations sur le contrôle de compte d’utilisateur et la Windows Installer, consultez [utilisation de Windows Installer avec UAC](using-windows-installer-with-uac.md) et [instructions pour les packages](guidelines-for-packages.md).

**Windows Installer 3,1, Windows Installer 3,0 et Windows Installer 2,0 :** Cette propriété est ignorée. Cette propriété est utilisée uniquement par Windows Installer 4,0 dans Windows Vista.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




