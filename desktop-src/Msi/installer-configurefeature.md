---
description: La méthode ConfigureFeature de l’objet installer configure l’état installé d’une fonctionnalité de produit.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configméthode ureFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 522dfffcbafd546dce218956729f01133708833a4a4c2732af3ea0248f87bc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632343"
---
# <a name="installerconfigurefeature-method"></a>Installer.Configméthode ureFeature

La méthode **ConfigureFeature** de l’objet [**installer**](installer-object.md) configure l’état installé d’une fonctionnalité de produit.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le code de produit du produit.

</dd> <dt>

*Fonctionnalité* 
</dt> <dd>

Spécifie l’ID de fonctionnalité de la fonctionnalité à configurer.

</dd> <dt>

*InstallState* 
</dt> <dd>

Spécifie l’état d’installation de la fonctionnalité. Ce paramètre doit avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                        | Signification                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | La fonctionnalité est publiée<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | La fonctionnalité est installée localement.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | La fonctionnalité est désinstallée.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | La fonctionnalité est installée pour s’exécuter à partir de la source.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | La fonctionnalité est installée à son emplacement par défaut.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[Fonctions d’installation et de configuration](installer-function-reference.md)
</dt> </dl>

 

 




