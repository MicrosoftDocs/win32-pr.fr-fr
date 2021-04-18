---
description: La propriété MSIDISABLERMRESTART détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés et redémarrés pour permettre l’installation de la mise à jour.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Propriété MSIDISABLERMRESTART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543216"
---
# <a name="msidisablermrestart-property"></a>Propriété MSIDISABLERMRESTART

La propriété **MSIDISABLERMRESTART** détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés et redémarrés pour permettre l’installation de la mise à jour.

## <a name="value"></a>Valeur



| Valeur                                                                        | Signification                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Tous les services système qui ont été arrêtés pour installer la mise à jour sont redémarrés. Toutes les applications qui se sont inscrites avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) sont redémarrées.<br/> |
| <dl> <dt>1</dt> </dl> | Les processus qui ont été arrêtés à l’aide du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) pendant l’installation de la mise à jour ne sont pas redémarrés après l’application de la mise à jour.<br/>                           |



 

## <a name="remarks"></a>Notes

La propriété **MSIDISABLERMRESTART** est ignorée si le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’est pas disponible ou est désactivé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
