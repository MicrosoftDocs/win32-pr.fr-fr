---
description: Les propriétés MSIINSTALLPERUSER et ALLUSERS peuvent être définies par l’utilisateur au moment de l’installation, par le biais de l’interface utilisateur ou sur une ligne de commande, pour demander que le Windows Installer installer un package à double usage pour l’utilisateur actuel ou tous les utilisateurs de l’ordinateur.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Propriété MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522778"
---
# <a name="msiinstallperuser-property"></a>Propriété MSIINSTALLPERUSER

Les propriétés **MSIINSTALLPERUSER** et [**ALLUSERS**](allusers.md) peuvent être définies par l’utilisateur au moment de l’installation, par le biais de l’interface utilisateur ou sur une ligne de commande, pour demander que le Windows Installer installer un package à double usage pour l’utilisateur actuel ou tous les utilisateurs de l’ordinateur. Pour utiliser la propriété **MSIINSTALLPERUSER** , la valeur de la propriété [**ALLUSERS**](allusers.md) doit être 2 et le package doit avoir été créé pour pouvoir être installé dans le contexte par utilisateur ou par ordinateur. Pour plus d’informations sur la création d’un package à double usage, consultez [création de package unique](single-package-authoring.md). Si la valeur de la propriété **ALLUSERS** n’est pas égale à 2, la valeur de la propriété **MSIINSTALLPERUSER** est ignorée et n’a aucun effet sur l’installation. La valeur de la propriété **MSIINSTALLPERUSER** est ignorée lors de l’installation du package à l’aide de Windows Installer 4,5 ou version antérieure.

Pour demander que le Windows Installer installer le package à double usage dans le [contexte d’installation](installation-context.md)par ordinateur, l’utilisateur peut définir la valeur de la propriété **MSIINSTALLPERUSER** sur une chaîne vide ("") et la valeur de la propriété [**ALLUSERS**](allusers.md) sur 2 à l’aide d’une interface utilisateur créée ou d’une ligne de commande.

Pour demander que le Windows Installer installer le package à double usage dans le [contexte d’installation](installation-context.md)par utilisateur, l’utilisateur peut définir la valeur de la propriété **MSIINSTALLPERUSER** sur 1 et la valeur de la propriété [**ALLUSERS**](allusers.md) sur 2 à l’aide d’une interface utilisateur créée ou d’une ligne de commande.

Si la valeur de la propriété [**ALLUSERS**](allusers.md) n’est pas égale à 2, le Windows Installer ignore la valeur de la propriété **MSIINSTALLPERUSER** . Si Windows Installer installe l’application dans le contexte par ordinateur, il réinitialise la valeur de la propriété **ALLUSERS** sur 1. Si Windows Installer installe l’application dans le contexte par utilisateur, il réinitialise la valeur de la propriété **ALLUSERS** sur une chaîne vide (""). Les applications qui ont été installées par utilisateur reçoivent par conséquent toutes les mises à jour ou réparations par utilisateur, ainsi que les mises à jour ou les réparations de réception par ordinateur installées par ordinateur.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** la propriété **MSIINSTALLPERUSER** est ignorée par les versions antérieures à Windows Installer 5,0.

## <a name="default-value"></a>Valeur par défaut

Le contexte d’installation par défaut recommandé est par utilisateur pour un package à double usage. Créez MSIINSTALLPERUSER = 1 et ALLUSERS = 2 dans la [table des propriétés](property-table.md) du package à double usage pour spécifier par utilisateur comme contexte d’installation par défaut.

## <a name="remarks"></a>Notes

Vous pouvez vous assurer que la propriété **MSIINSTALLPERUSER** n’a pas été définie en définissant sa valeur sur une chaîne vide (""), MSIINSTALLPERUSER = "".

Le contexte d’installation détermine les valeurs des propriétés [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)et [**CommonFiles64Folder**](commonfiles64folder.md) . Le contexte d’installation détermine les parties du registre où les entrées de la [table du Registre](registry-table.md) et de la [table RemoveRegistry](removeregistry-table.md), avec-1 dans la colonne racine, sont écrites ou supprimées. Pour plus d’informations sur le contexte d’installation, consultez [contexte d’installation](installation-context.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[Contexte d’installation](installation-context.md)
</dt> <dt>

[Création d’un package unique](single-package-authoring.md)
</dt> </dl>

 

 




