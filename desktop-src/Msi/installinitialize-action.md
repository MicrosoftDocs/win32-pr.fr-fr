---
description: L’action InstallInitialize et l’action InstallFinalize marquent le début et la fin d’une séquence d’actions qui modifient le système.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Action InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012038"
---
# <a name="installinitialize-action"></a>Action InstallInitialize

L’action InstallInitialize et l’action [InstallFinalize](installfinalize-action.md) marquent le début et la fin d’une séquence d’actions qui modifient le système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallInitialize doit être séquencée avant toute action qui modifie le système, telle que l’action [InstallFiles](installfiles-action.md) , l’action [WriteRegistryValues](writeregistryvalues-action.md) , l’action [SelfRegModules](selfregmodules-action.md) et l’action [ProcessComponents](processcomponents-action.md) . L’action InstallInitialize doit donc être séquencée avant l’action [InstallFinalize](installfinalize-action.md) et l’action [InstallExecute](installexecute-action.md) .

les [actions personnalisées](custom-actions.md) qui modifient le package Windows Installer, par exemple en ajoutant des lignes à une table qui gère des ressources installables, telles que la table [du registre](registry-table.md) ou la table [DuplicateFile](duplicatefile-table.md) , doivent être séquencées avant l’action InstallInitialize.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

 

 



