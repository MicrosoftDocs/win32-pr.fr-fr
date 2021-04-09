---
description: L’action BindImage lie chaque exécutable ou DLL qui doit être lié aux dll importées par celui-ci.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Action BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864438"
---
# <a name="bindimage-action"></a>Action BindImage

L’action BindImage lie chaque exécutable ou DLL qui doit être lié aux dll importées par celui-ci. L’action BindImage agit sur chaque fichier de la table [BindImage](bindimage-table.md) , mais uniquement sur ceux qui doivent être installés localement. Le programme d’installation calcule l’adresse virtuelle de chaque fonction importée à partir de toutes les dll, puis enregistre l’adresse virtuelle calculée dans la [*table d’adresses d’importation*](i-gly.md) (IAT) de l’image d’importation.

L’action BindImage appelle en interne l’API Windows **BindImageEx** .

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action BindImage doit venir après l’action [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action     |
|-------|--------------------------------|
| \[1\] | Identificateur de fichier de l’exécutable. |



 

 

 



