---
description: L’action d’installation est une action de niveau supérieur appelée pour installer ou supprimer des composants.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Action d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5f648084b7386465f6bb59dd6b523cb51489e4cb83677c0b5cb47fe845be42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810999"
---
# <a name="install-action"></a>Action d’installation

L’action d’installation est une action de niveau supérieur appelée pour installer ou supprimer des composants. Cette action interroge la table [InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md) pour l’action à exécuter, la condition d’exécution de l’action et la place de l’action dans la séquence :

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

l’action d’installation n’est pas appelée à partir de la séquence de la table d’action, elle est passée à Windows Installer quand [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé, ou l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande «**/i**», ou lorsqu’une fonction de programme d’installation est appelée et peut exécuter une tâche d’installation, telle que [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)ou [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



