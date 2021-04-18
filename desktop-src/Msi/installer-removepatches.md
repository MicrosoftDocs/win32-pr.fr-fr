---
description: La méthode RemovePatches supprime un ou plusieurs correctifs pour les produits éligibles pour recevoir le correctif. La méthode RemovePatches appelle MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer. RemovePatches, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533103"
---
# <a name="installerremovepatches-method"></a>Installer. RemovePatches, méthode

La méthode **RemovePatches** supprime un ou plusieurs correctifs pour les produits éligibles pour recevoir le correctif. La méthode **RemovePatches** appelle [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).

## <a name="syntax"></a>Syntaxe


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PatchList* 
</dt> <dd>

Chaîne qui contient une liste délimitée par des points-virgules des correctifs à supprimer. Chaque correctif peut être représenté soit par le chemin d’accès complet au package de correctifs, soit par le GUID du correctif. Ce paramètre est obligatoire.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Chaîne contenant le GUID du produit à partir duquel les correctifs doivent être supprimés. Ce paramètre est obligatoire.

</dd> <dt>

*UninstallType* 
</dt> <dd>

Valeur entière qui spécifie le type de suppression de correctif logiciel. Ce paramètre doit être **msiInstallTypeSingleInstance**.

</dd> <dt>

*PropertyList* 
</dt> <dd>

Chaîne qui spécifie les paires propriété = valeur à inclure. Ce paramètre est facultatif.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Consultez [désinstallation des correctifs](uninstalling-patches.md) pour obtenir un exemple qui montre comment une application peut supprimer un correctif de tous les produits disponibles pour l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Désinstallation des correctifs](uninstalling-patches.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




