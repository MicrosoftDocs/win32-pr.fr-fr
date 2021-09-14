---
description: L’action MsiPublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Action MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119709"
---
# <a name="msipublishassemblies-action"></a>Action MsiPublishAssemblies

L’action MsiPublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32. L’action interroge la [table MsiAssembly](msiassembly-table.md) pour déterminer les assemblys qui ont des fonctionnalités publiées ou installées dans le global assembly cache et les assemblys dont le composant parent est publié ou installé dans un emplacement isolé pour une application particulière. Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).

sur les systèmes Microsoft Windows XP et versions ultérieures, Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md). Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action MsiPublishAssemblies doit venir après l' [action InstallInitialize](installinitialize-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md) ou la [table AdvtExecuteSequence](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Contexte de l’application.       |
| \[2\] | Nom de l’assembly :             |



 

## <a name="remarks"></a>Notes

Pour plus d’informations, consultez [assemblys](assemblies.md).

L' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md) gère la publication des assemblys en cours de suppression.

 

 
