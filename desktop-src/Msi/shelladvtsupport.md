---
description: La propriété ShellAdvtSupport est définie par le programme d’installation si l’interface IShellLink du système prend en charge la résolution du descripteur du programme d’installation.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propriété ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfacc34bfffdde9ce34841030f38c443a243c9923cb70749a27615cccc1c676e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628439"
---
# <a name="shelladvtsupport-property"></a>Propriété ShellAdvtSupport

La propriété **ShellAdvtSupport** est définie par le programme d’installation si l’interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) du système prend en charge la résolution du descripteur du programme d’installation.

## <a name="remarks"></a>Remarques

Si cette propriété est définie, l’interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) du système prend en charge la résolution du descripteur du programme d’installation. cela est pris en charge par Windows 2000 et les systèmes exécutant Internet Explorer 4,01. Si cette propriété n’est pas définie, le programme d’installation a le comportement par défaut de création de fonctionnalités non publiées lors de l’installation, soit localement, soit à partir de la source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Prise en charge des plateformes de la publication](platform-support-of-advertisement.md)
</dt> </dl>

 

 
