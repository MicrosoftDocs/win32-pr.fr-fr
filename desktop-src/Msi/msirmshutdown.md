---
description: La propriété MSIRMSHUTDOWN détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés pour permettre l’installation de la mise à jour.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Propriété MSIRMSHUTDOWN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119697"
---
# <a name="msirmshutdown-property"></a>Propriété MSIRMSHUTDOWN

La propriété **MSIRMSHUTDOWN** détermine la manière dont les applications ou services qui utilisent actuellement des fichiers affectés par une mise à jour doivent être arrêtés pour permettre l’installation de la mise à jour.

## <a name="value"></a>Valeur



| Valeur                                                                        | Signification                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Les processus ou services qui utilisent actuellement des fichiers affectés par la mise à jour sont arrêtés.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Les processus ou services qui utilisent actuellement des fichiers affectés par la mise à jour et qui ne répondent pas au [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md)sont forcés à s’arrêter.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Les processus ou services qui utilisent actuellement des fichiers affectés par la mise à jour sont arrêtés uniquement s’ils ont tous été inscrits pour un redémarrage. Si un processus ou un service n’a pas été inscrit pour un redémarrage, aucun processus ou service n’est arrêté.<br/> |



 

## <a name="remarks"></a>Notes

La propriété **MSIRMSHUTDOWN** est ignorée si le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’est pas disponible ou est désactivé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
