---
description: L’action RMCCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Action RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d18431a6806d055c824bf51331d6390a6f669100aa9a33db9665b9d7b37008c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625898"
---
# <a name="rmccpsearch-action"></a>Action RMCCPSearch

L’action RMCCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RMCCPSearch doit être créée dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md). Le programme d’installation empêche RMCCPSearch de s’exécuter dans la séquence InstallExecuteSequence si l’action a déjà été exécutée dans la séquence InstallUISequence.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

L’action RMCCPSearch nécessite que la propriété [**\_ lecteur CCP**](ccp-drive.md) soit définie sur le chemin d’accès racine sur le [*volume*](v-gly.md) amovible qui a l’installation de l’un des produits éligibles.

Chaque signature de fichier de la table CCPSearch est recherchée dans le chemin d’accès référencé par la propriété [**\_ lecteur CCP**](ccp-drive.md) à l’aide de la table [DrLocator](drlocator-table.md) . L’absence de signature à partir de la table de [signature](signature-table.md) désigne un répertoire. Si une signature est identifiée comme existante, l’action RMCCPSearch se termine.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table CCPSearch](ccpsearch-table.md)
</dt> </dl>

 

 



