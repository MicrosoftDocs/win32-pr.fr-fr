---
description: Un demandeur doit sélectionner un fournisseur spécifique uniquement s’il contient des informations sur les fournisseurs disponibles.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Sélection des fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115139"
---
# <a name="selecting-providers"></a>Sélection des fournisseurs

Un demandeur doit sélectionner un fournisseur spécifique uniquement s’il contient des informations sur les fournisseurs disponibles.

Dans la mesure où cela n’est généralement pas le cas, il est recommandé qu’un demandeur fournisse \_ la valeur NULL comme ID de fournisseur à [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), ce qui permet au système de choisir un fournisseur selon l’algorithme suivant :

1.  Si un fournisseur de matériel qui prend en charge le volume donné est disponible, il est sélectionné.
2.  Si aucun fournisseur de matériel n’est disponible, si un fournisseur de logiciels spécifique au volume donné est disponible, il est sélectionné.
3.  Si aucun fournisseur de matériel et aucun fournisseur de logiciels spécifique aux volumes n’est disponible, le fournisseur système est sélectionné.

Toutefois, un demandeur peut obtenir des informations sur les fournisseurs disponibles à l’aide de [**IVssBackupComponents :: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query). Avec ces informations, et seulement si l’application de sauvegarde a une bonne compréhension des différents fournisseurs, un demandeur peut fournir un ID de fournisseur valide à [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Notez que tous les volumes n’ont pas besoin d’avoir le même fournisseur.

 

 



