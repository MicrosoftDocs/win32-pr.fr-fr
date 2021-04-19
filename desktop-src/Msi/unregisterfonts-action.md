---
description: L’action UnregisterFonts supprime les informations d’inscription relatives aux polices installées du système.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Action UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535060"
---
# <a name="unregisterfonts-action"></a>Action UnregisterFonts

L’action UnregisterFonts supprime les informations d’inscription relatives aux polices installées du système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [RemoveFiles](removefiles-action.md) doit être appelée après UnregisterFonts.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Fichier de police.                 |



 

## <a name="remarks"></a>Notes

L’action UnregisterFonts est exécutée si le fichier spécifié dans la \_ colonne file de la [table font](font-table.md) appartient à un composant en cours de désinstallation.

 

 



