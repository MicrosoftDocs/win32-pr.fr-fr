---
description: Le programme d’installation définit la propriété RedirectedDLLSupport si la plateforme système effectuant l’installation prend en charge les composants isolés.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propriété RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24da5990645d4c27120c3a010cc517475ba6e706c2fb41d69a024d15ca524549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979319"
---
# <a name="redirecteddllsupport-property"></a>Propriété RedirectedDLLSupport

Le programme d’installation définit la propriété **RedirectedDLLSupport** si la plateforme système effectuant l’installation prend en charge les [composants isolés](isolated-components.md).

Le programme d’installation affecte à la propriété **RedirectedDLLSupport** la valeur 1 si le système effectuant l’installation prend en charge les [composants isolés](isolated-components.md) basés sur. Fichiers locaux. Le programme d’installation définit la propriété **RedirectedDLLSupport** sur la valeur 2 si le système qui exécute l’installation prend en charge l’isolation à l’aide de l’une ou l’autre. Des fichiers locaux ou des assemblys Win32 côte à côte.

La propriété **RedirectedDLLSupport** peut être utilisée pour conditionner l' [action IsolateComponents](isolatecomponents-action.md) dans la [table InstallUISequence](installuisequence-table.md) ou la [table InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




