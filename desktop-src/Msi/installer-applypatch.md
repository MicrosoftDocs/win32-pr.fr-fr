---
description: Pour chaque produit indiqué par le package de correctifs comme éligibles pour recevoir le correctif, la méthode ApplyPatch de l’objet installer appelle une installation et définit la propriété PATCH sur le chemin d’accès du package correctif.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer. ApplyPatch, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c4bcb1ba1dc988f3c28188b4b448dba611b83c6cffbe7f942710569ac089776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633226"
---
# <a name="installerapplypatch-method"></a>Installer. ApplyPatch, méthode

Pour chaque produit indiqué par le package de correctifs comme éligibles pour recevoir le correctif, la méthode **ApplyPatch** de l’objet [**installer**](installer-object.md) appelle une installation et définit la propriété [**patch**](patch.md) sur le chemin d’accès du package correctif.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PatchPackage* 
</dt> <dd>

Spécifie un chemin d’accès au package de correctifs.

</dd> <dt>

*InstallPackage* 
</dt> <dd>

Si *InstallType* a la valeur MsiInstallTypeNetworkImage, *INSTALLPACKAGE* spécifie le chemin d’accès au produit qui doit être corrigé. Si *InstallType* a la valeur msiInstallTypeDefault et que *INSTALLPACKAGE* a la valeur 0, le programme d’installation applique le correctif à tous les produits éligibles figurant dans le package de correctifs.

Si *InstallType* est msiInstallTypeSingleInstance, le programme d’installation applique le correctif au produit spécifié par *INSTALLPACKAGE*. Dans ce cas, les autres produits éligibles répertoriés dans le package de correctifs sont ignorés et le paramètre *INSTALLPACKAGE* contient la chaîne terminée par le caractère null qui représente le code de produit de l’instance à corriger. ce type d’installation requiert la version de Windows Installer fournie avec le Windows Server 2003 ou version ultérieure, ou Windows Installer XP SP1 ou version ultérieure.

</dd> <dt>

*InstallType (type d'installation)* 
</dt> <dd>

Ce paramètre spécifie le type d’installation à corriger. Le paramètre *InstallType* est ignoré si *INSTALLPACKAGE* est omis.



| Valeur                                                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Indique une installation administrative. Dans ce cas, *INSTALLPACKAGE* doit être défini sur un chemin d’accès de package. La valeur 1 pour msiInstallTypeNetworkImage spécifie une installation d’administration.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Recherche des produits à corriger dans le système. Dans ce cas, *INSTALLPACKAGE* doit être une chaîne vide.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Correction du produit spécifié par *INSTALLPACKAGE*. *INSTALLPACKAGE* est le code du produit de l’instance à corriger. ce type d’installation requiert la version de Windows Installer fournie avec Windows Server 2003 ou version ultérieure, ou Windows Installer XP SP1 ou version ultérieure. Pour plus d’informations, consultez [installation de plusieurs instances de produits et correctifs](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Spécifie les paramètres de propriété définis sur la ligne de commande. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Étant donné que le délimiteur de liste pour les transformations, les sources et les correctifs est un point-virgule, ce caractère ne doit pas être utilisé pour les noms de fichiers ou les chemins d’accès.

La propriété de [**réinstallation**](reinstall.md) est requise lors de l’application d’une [petite mise à jour](small-updates.md) ou d’un correctif de [mise à niveau mineur](minor-upgrades.md) . Sans cette propriété, le correctif est inscrit sur le système, mais ne peut pas mettre à jour les fichiers.

**Windows Installer 2,0 :** Vous devez définir la propriété [**réinstaller**](reinstall.md) sur la ligne de commande lors de l’application d’une [petite mise à jour](small-updates.md) ou d’un correctif de [mise à niveau mineure](minor-upgrades.md) . Pour les correctifs qui n’utilisent pas de [type d’action personnalisé 51](custom-action-type-51.md) pour définir automatiquement les propriétés **REINSTALL** et [**REINSTALLMODE**](reinstallmode.md) , la propriété **REINSTALL** doit être définie explicitement à l’aide du paramètre *CommandLine* . Définissez la propriété **réinstaller** pour répertorier les fonctionnalités affectées par le correctif ou utilisez un paramètre par défaut pratique « réinstaller = All ». La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».

**Windows Installer 3,0 et versions ultérieures :** à partir de Windows Installer version 3,0, la propriété de [**réinstallation**](reinstall.md) est configurée par le programme d’installation et n’a pas besoin d’être définie sur la ligne de commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




