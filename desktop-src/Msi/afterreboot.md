---
description: Le programme d’installation affecte la valeur 1 à la propriété AFTERREBOOT après un redémarrage appelé par l’action ForceReboot. Le programme d’installation ajoute AFTERREBOOT = 1 à la ligne de commande exécutée immédiatement après le redémarrage.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propriété AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8fb80a3d8ff167f93aab6c95fc3eadb8b5312daf9d2a2856f01cb7d01ee383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145912"
---
# <a name="afterreboot-property"></a>Propriété AFTERREBOOT

Le programme d’installation affecte la valeur 1 à la propriété **AFTERREBOOT** après un redémarrage appelé par l' [action ForceReboot](forcereboot-action.md). Le programme d’installation ajoute AFTERREBOOT = 1 à la ligne de commande exécutée immédiatement après le redémarrage.

## <a name="remarks"></a>Remarques

L' [action ForceReboot](forcereboot-action.md) doit toujours être utilisée avec une instruction conditionnelle de sorte que le programme d’installation déclenche un redémarrage uniquement lorsque cela est nécessaire. Un redémarrage peut être nécessaire si un fichier particulier a été remplacé ou si un composant particulier a été installé. Le cas est différent pour chaque produit et une action personnalisée peut être nécessaire pour déterminer si un redémarrage est nécessaire. La condition sur l’action ForceReboot utilise généralement la propriété **AFTERREBOOT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Redémarrages du système](system-reboots.md)
</dt> </dl>

 

 




