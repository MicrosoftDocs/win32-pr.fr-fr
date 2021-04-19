---
description: L’action InstallSFPCatalogFile installe les catalogues utilisés par Windows me pour la protection des fichiers Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Action InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513359"
---
# <a name="installsfpcatalogfile-action"></a>Action InstallSFPCatalogFile

L’action InstallSFPCatalogFile installe les catalogues utilisés par Windows me pour la protection des fichiers Windows. InstallSFPCatalogFile interroge la table de [composants](component-table.md), la [table de fichiers](file-table.md), la table [FileSFPCatalog](filesfpcatalog-table.md) et la [table SFPCatalog](sfpcatalog-table.md). Les catalogues sont installés s’ils sont associés à un fichier dans un composant qui est défini pour une installation locale ou s’ils sont associés à un fichier en cours de réparation dans un composant installé localement.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallSFPCatalogFile doit être séquencée avant [InstallFiles](installfiles-action.md) et après [CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nom du catalogue en cours d’installation.                          |
| \[2\] | Nom du catalogue dont l’installation du catalogue dépend. |



 

## <a name="remarks"></a>Notes

Catalogue dépendant d’un autre catalogue installé après le catalogue parent.

 

 



