---
description: Affectez la valeur 1 à la propriété MSIUNINSTALLSUPERSEDEDCOMPONENTS dans la table de propriétés ou sur une ligne de commande.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propriété MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540001"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Propriété MSIUNINSTALLSUPERSEDEDCOMPONENTS

Affectez la valeur 1 à la propriété **MSIUNINSTALLSUPERSEDEDCOMPONENTS** dans la [table de propriétés](property-table.md) ou sur une ligne de commande. Lorsque cette propriété a la valeur 1, le programme d’installation détermine si les composants de tous les correctifs remplacés sont devenus redondants. Le programme d’installation peut annuler l’inscription et désinstaller les composants redondants pour empêcher la conservation des composants orphelins sur l’ordinateur.

La définition de cette propriété affecte les composants de tous les correctifs remplacés. Pour activer cette fonctionnalité pour des composants uniques, utilisez l’attribut **msidbComponentAttributesUninstallOnSupersedence** dans la [table des composants](component-table.md).

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge. Les versions antérieures à Windows Installer 4,5 ignorent la propriété **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,5 ou Windows Installer 4,5 sur Windows Vista, Windows XP, Windows Server 2003 et Windows Server 2008. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




