---
description: L’action UnregisterFonts supprime les informations d’inscription relatives aux polices installées du système.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Action UnregisterFonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786999"
---
# <a name="unregisterfonts-action"></a>Action UnregisterFonts

L’action UnregisterFonts supprime les informations d’inscription relatives aux polices installées du système.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action [RemoveFiles](removefiles-action.md) doit être appelée après UnregisterFonts.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Fichier de police.                 |



 

## <a name="remarks"></a>Remarques

L’action UnregisterFonts est exécutée si le fichier spécifié dans la \_ colonne file de la [table font](font-table.md) appartient à un composant en cours de désinstallation.

 

 



