---
description: La méthode ConfigureProduct de l’objet installer installe ou désinstalle un produit.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configméthode ureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fd64424105bc06364abf2b047ba4d986fdd5540d007109dfb9fdc087250c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632156"
---
# <a name="installerconfigureproduct-method"></a>Installer.Configméthode ureProduct

La méthode **ConfigureProduct** de l’objet [**installer**](installer-object.md) installe ou désinstalle un produit.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le code de produit du produit.

</dd> <dt>

*InstallLevel* 
</dt> <dd>

Spécifie la configuration d’installation par défaut du produit. Le paramètre InstallLevel est ignoré et toutes les fonctionnalités sont installées si le paramètre InstallState est défini sur une autre valeur que msiInstallStateDefault.

Ce paramètre doit avoir la valeur 0 (installation à l’aide des niveaux de fonctionnalité créés), 65535 (installer toutes les fonctionnalités) ou une valeur comprise entre 0 et 65535 pour installer un sous-ensemble des fonctionnalités disponibles.

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

## <a name="remarks"></a>Remarques

La méthode **ConfigureProduct** affiche l’interface utilisateur à l’aide des paramètres actuels. Les paramètres de l’interface utilisateur peuvent être modifiés en modifiant la [**propriété UILevel (objet programme d’installation)**](installer-uilevel.md) avant d’appeler la méthode **ConfigureProduct** .

Si le paramètre *InstallState* est défini sur une autre valeur que msiInstallStateDefault, le paramètre *InstallLevel* est ignoré et toutes les fonctionnalités du produit sont installées. Utilisez la méthode [**ConfigureFeature**](installer-configurefeature.md) pour contrôler l’installation de fonctionnalités individuelles lorsque le paramètre *InstallState* n’a pas la valeur msiInstallStateDefault.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Fonctions d’installation et de configuration](installer-function-reference.md)
</dt> </dl>

 

 




