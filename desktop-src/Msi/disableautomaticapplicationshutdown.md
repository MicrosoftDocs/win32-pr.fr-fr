---
description: Si cette stratégie système par ordinateur est définie sur 1 (un), Windows Installer n’interagit pas avec le gestionnaire de redémarrage, mais elle utilisera la boîte de dialogue FilesInUse. Si cette stratégie système par ordinateur est définie sur 2 (deux), Windows Installer utilise la boîte de dialogue FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519637"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

Si cette stratégie système par ordinateur est définie sur 1 (un), Windows Installer n’interagit pas avec le [Gestionnaire de redémarrage](/windows/desktop/RstMgr/restart-manager-portal), mais elle utilisera la [boîte de dialogue FilesInUse](filesinuse-dialog.md).

Si cette stratégie système par ordinateur est définie sur 2 (deux), Windows Installer utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md). Ce paramètre désactive les tentatives du gestionnaire de [redémarrage](/windows/desktop/RstMgr/restart-manager-portal) afin d’atténuer les redémarrages lors de l’installation d’un Windows Installer Package qui n’a pas été créé pour utiliser le gestionnaire de redémarrage. Le programme d’installation utilise toujours le gestionnaire de redémarrage pour détecter les fichiers utilisés par les applications.

La stratégie DisableAutomaticApplicationShutdown est disponible à partir de Windows Installer version 4,0 sur Windows Vista.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
