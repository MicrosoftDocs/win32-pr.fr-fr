---
description: Le programme d’installation définit la propriété RedirectedDLLSupport si la plateforme système effectuant l’installation prend en charge les composants isolés.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propriété RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523643"
---
# <a name="redirecteddllsupport-property"></a>Propriété RedirectedDLLSupport

Le programme d’installation définit la propriété **RedirectedDLLSupport** si la plateforme système effectuant l’installation prend en charge les [composants isolés](isolated-components.md).

Le programme d’installation affecte à la propriété **RedirectedDLLSupport** la valeur 1 si le système effectuant l’installation prend en charge les [composants isolés](isolated-components.md) basés sur. Fichiers locaux. Le programme d’installation définit la propriété **RedirectedDLLSupport** sur la valeur 2 si le système qui exécute l’installation prend en charge l’isolation à l’aide de l’une ou l’autre. Des fichiers locaux ou des assemblys Win32 côte à côte.

La propriété **RedirectedDLLSupport** peut être utilisée pour conditionner l' [action IsolateComponents](isolatecomponents-action.md) dans la [table InstallUISequence](installuisequence-table.md) ou la [table InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




