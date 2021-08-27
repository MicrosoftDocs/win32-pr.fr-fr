---
description: L’action MsiUnpublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32 en cours de suppression.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Action MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f640338e13f53b115ca3b93aa2a63987efb5aa7cf053d4c8a59d8d20d0f7e3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943896"
---
# <a name="msiunpublishassemblies-action"></a>Action MsiUnpublishAssemblies

L’action MsiUnpublishAssemblies gère la publication d’assemblys common language runtime et d’assemblys Win32 en cours de suppression. L’action interroge la [table MsiAssembly](msiassembly-table.md) pour déterminer les assemblys pour lesquels des fonctionnalités publiées ou installées ont été supprimées de la global assembly cache et quels assemblys ont un composant parent publié ou installé en cours de suppression d’un emplacement isolé pour une application particulière. Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).

sur les systèmes exécutant Windows XP et versions ultérieures, Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md). Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action MsiUnpublishAssemblies doit venir après l' [action InstallInitialize](installinitialize-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Contexte de l’application.       |
| \[2\] | Nom de l’assembly :             |



 

## <a name="remarks"></a>Remarques

L' [action MsiPublishAssemblies](msipublishassemblies-action.md) gère la publication des assemblys publiés ou installés.

 

 
