---
description: Les actions personnalisées sont appelées de la même façon que les actions standard, soit par appel explicite, soit lors de l’exécution d’une table de séquences.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Appel d’actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012000"
---
# <a name="invoking-custom-actions"></a>Appel d’actions personnalisées

Les actions personnalisées sont appelées de la même façon que les actions standard, soit par appel explicite, soit lors de l’exécution d’une table de séquences. Il existe deux méthodes pour appeler des actions :

-   Vous appelez l’action spécifiée directement avec la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .
-   Une action de niveau supérieur appelle la table Sequence contenant l’action personnalisée. Pour plus d’informations sur la planification d’une action personnalisée dans une table de séquences, consultez [séquencement des actions personnalisées](sequencing-custom-actions.md).

Quand le programme d’installation obtient un nom d’action à partir de la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) , ou d’une table de séquence, il commence par Rechercher une action standard portant ce nom. S’il ne trouve pas l’action standard, le programme d’installation interroge la [table CustomAction](customaction-table.md) pour vérifier si l’action spécifiée est une action personnalisée. Si l’action spécifiée n’est pas une action personnalisée, le programme d’installation interroge la [table de boîtes de dialogue](dialog-table.md) pour obtenir une boîte de dialogue.

 

 



