---
description: La propriété PatchProperty obtient des informations sur un correctif spécifique appliqué à une instance spécifique du produit. Cette propriété appelle MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Méthode patch. PatchProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123670"
---
# <a name="patchpatchproperty-method"></a>Méthode patch. PatchProperty

La propriété **PatchProperty** obtient des informations sur un correctif spécifique appliqué à une instance spécifique du produit. Cette propriété appelle [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

## <a name="syntax"></a>Syntaxe


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szProperty* 
</dt> <dd>

Le paramètre *szProperty* peut avoir l’une des valeurs suivantes.



| Nom          | Signification                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | Obtient le fichier correctif mis en cache utilisé par le produit.                                                                                                                                                                                                                                                                               |
| Transformations    | Obtient l’ensemble des transformations de correctifs appliquées au produit par la dernière installation de correctif logiciel. Cette valeur peut ne pas être disponible pour les applications non gérées par utilisateur si l’utilisateur n’est pas connecté à l’ordinateur.                                                                                                                     |
| InstallDate   | Obtient la date à laquelle le correctif a été appliqué au produit.                                                                                                                                                                                                                                                                      |
| Non installables | Retourne « 1 » si le correctif est marqué comme possible pour la désinstallation du produit. Dans ce cas, le programme d’installation peut toujours bloquer la désinstallation si ce correctif est requis par un autre correctif qui ne peut pas être désinstallé.                                                                                                          |
| State         | Retourne « 1 » si ce correctif est actuellement appliqué au produit. Retourne « 2 » si ce correctif logiciel a été remplacé par un autre correctif. Retourne « 4 » si ce correctif a été rendu obsolète par un autre correctif. Ces valeurs correspondent aux constantes utilisées par le paramètre *dwFilter* de [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa). |
| DisplayName   | Obtient le nom complet inscrit pour le correctif. Pour les correctifs qui n’incluent pas la propriété DisplayName dans la table [MsiPatchMetadata](msipatchmetadata-table.md) , le nom complet retourné est une chaîne vide ("").                                                                                                      |
| MoreInfoURL   | Obtenir l’URL des informations de support inscrites pour le correctif. Pour les correctifs qui n’incluent pas la propriété MoreInfoURL dans la table [MsiPatchMetadata](msipatchmetadata-table.md) , l’URL des informations de prise en charge retournées est une chaîne vide ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode peut retourner \_ une erreur Unknown \_ patch, si l’objet [**patch**](patch-object.md) est initialisé avec une chaîne vide pour *ProductCode*.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Correctif**](patch-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




