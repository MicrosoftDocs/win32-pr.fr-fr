---
description: L’action RegisterFonts inscrit les polices installées auprès du système. Cette action mappe le nom de police dans la colonne FontTitle de la table de polices au chemin d’accès du fichier de polices installé.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: Action RegisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518239"
---
# <a name="registerfonts-action"></a>Action RegisterFonts

L’action RegisterFonts inscrit les polices installées auprès du système. Cette action mappe le nom de police dans la colonne FontTitle de la [table de polices](font-table.md) au chemin d’accès du fichier de polices installé.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [InstallFiles](installfiles-action.md) doit être appelée avant d’appeler l’action RegisterFonts.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Fichier de police.                 |



 

## <a name="remarks"></a>Notes

L’action RegisterFonts est exécutée si le fichier spécifié dans la \_ colonne fichier de la [table de polices](font-table.md) appartient à un composant en cours d’installation.

 

 



