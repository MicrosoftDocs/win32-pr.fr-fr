---
description: Pour désactiver l’interface utilisateur incorporée pour l’installation définie dans la table MsiEmbeddedUI, affectez la valeur 1 à la propriété MSIDISABLEEEUI sur la ligne de commande.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propriété MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e599ed0786c7d2c55644eb5759db3917757d3b41f6107161d72a3cc559484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039949"
---
# <a name="msidisableeeui-property"></a>Propriété MSIDISABLEEEUI

Pour désactiver l’interface utilisateur incorporée pour l’installation définie dans la [table MsiEmbeddedUI](msiembeddedui-table.md), affectez la valeur 1 à la propriété MSIDISABLEEEUI sur la ligne de commande.

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge. les Versions antérieures à Windows Installer 4,5 ignorent la propriété MSIDISABLEEEUI.

## <a name="remarks"></a>Remarques

Dans une installation de plusieurs packages, un package enfant doit généralement utiliser l’interface utilisateur du package parent et ne pas initialiser sa propre interface utilisateur incorporée. Si la propriété MSIDISABLEEEUI n’est pas définie dans le package parent, le package enfant utilise l’interface utilisateur incorporée du package parent par défaut et ignore la propriété MSIDISABLEEEUI dans le package enfant.

La propriété MSIDISABLEEEUI désactive l’interface utilisateur incorporée pour un package unique. Vous pouvez utiliser la stratégie [MsiDisableEmbeddedUI](msidisableembeddedui.md) pour désactiver les interfaces utilisateur incorporées pour tous les packages sur l’ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,5 sur Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




