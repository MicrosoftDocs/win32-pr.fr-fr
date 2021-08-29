---
description: La propriété UpgradeCode est un GUID qui représente un ensemble connexe de produits. La fonction UpgradeCode est utilisée dans la table de mise à niveau pour rechercher les versions associées du produit qui sont déjà installées. Cette propriété est utilisée par l’action RegisterProduct.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e42253dfe0466636783603f6b5098425503a9f0984363e11d4c7241b17a191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809659"
---
# <a name="upgradecode-property"></a>UpgradeCode, propriété

La propriété **UpgradeCode** est un GUID qui représente un ensemble connexe de produits. La fonction **UpgradeCode** est utilisée dans la [table de mise à niveau](upgrade-table.md) pour rechercher les versions associées du produit qui sont déjà installées.

Cette propriété est utilisée par l' [action RegisterProduct](registerproduct-action.md).

## <a name="remarks"></a>Remarques

Il est fortement recommandé que les auteurs des packages d’installation spécifient une **UpgradeCode** pour leur application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Correctifs et mises à niveau](patching-and-upgrades.md)
</dt> <dt>

[Préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




