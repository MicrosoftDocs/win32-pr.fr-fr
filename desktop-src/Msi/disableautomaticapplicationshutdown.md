---
description: si cette stratégie système par ordinateur est définie sur 1 (un), Windows Installer n’interagit pas avec le gestionnaire de redémarrage, mais elle utilisera la boîte de dialogue FilesInUse. si cette stratégie système par ordinateur est définie sur 2 (deux), Windows Installer utilise la boîte de dialogue FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091537"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

si cette stratégie système par ordinateur est définie sur 1 (un), Windows Installer n’interagit pas avec le [gestionnaire de redémarrage](/windows/desktop/RstMgr/restart-manager-portal), mais elle utilisera la [boîte de dialogue FilesInUse](filesinuse-dialog.md).

si cette stratégie système par ordinateur est définie sur 2 (deux), Windows Installer utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md). ce paramètre désactive les tentatives du gestionnaire de [redémarrage](/windows/desktop/RstMgr/restart-manager-portal) afin d’atténuer les redémarrages lors de l’installation d’un Windows Installer package qui n’a pas été créé pour utiliser le gestionnaire de redémarrage. Le programme d’installation utilise toujours le gestionnaire de redémarrage pour détecter les fichiers utilisés par les applications.

la stratégie DisableAutomaticApplicationShutdown est disponible à partir de Windows Installer version 4,0 sur Windows Vista.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
