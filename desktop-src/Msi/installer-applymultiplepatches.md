---
description: La méthode ApplyMultiplePatches applique un ou plusieurs correctifs aux produits qui peuvent recevoir le correctif. La méthode définit la propriété PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer. ApplyMultiplePatches, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633206"
---
# <a name="installerapplymultiplepatches-method"></a>Installer. ApplyMultiplePatches, méthode

La méthode **ApplyMultiplePatches** applique un ou plusieurs correctifs aux produits qui peuvent recevoir le correctif. La méthode définit la propriété [**patch**](patch.md) .

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PatchPackagesList* 
</dt> <dd>

Chaîne qui contient une liste délimitée par des points-virgules des chemins d’accès aux fichiers correctifs. par exemple : "" c : \\ \\ cache de téléchargement sus \\ \\ Office \\ sp1. msp ; c : \\ sus \\ download \\ cache \\ Office \\ QFE1. msp ; c : \\ sus \\ download \\ cache \\ Office \\ QFEn. msp ""

</dd> <dt>

*Produit* 
</dt> <dd>

Ce paramètre fournit le [**ProductCode**](productcode.md) du produit en cours de correction. Ce paramètre est facultatif. Lorsque ce paramètre a la valeur null, les correctifs sont appliqués à tous les produits qui sont éligibles à la réception de ces correctifs.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Chaîne terminée par le caractère null qui spécifie les paramètres de propriété de ligne de commande. Ce paramètre est facultatif. Consultez [à propos des propriétés](about-properties.md) et [définition des valeurs de propriété publiques sur la ligne de commande](setting-public-property-values-on-the-command-line.md). Ces propriétés sont partagées par tous les produits cibles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**CORRECTIF**](patch.md)
</dt> <dt>

[Définition des valeurs de propriété publiques sur la ligne de commande](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




