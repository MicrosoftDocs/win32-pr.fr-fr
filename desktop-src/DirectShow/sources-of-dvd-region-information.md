---
description: Sources d’informations sur les régions DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Sources d’informations sur les régions DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952417"
---
# <a name="sources-of-dvd-region-information"></a>Sources d’informations sur les régions DVD

Il existe trois sources d’informations de région de DVD qui fonctionnent ensemble pour déterminer la région de lecture des DVD sur un PC Windows.

-   Titre du DVD. La plupart des titres de DVD sont marqués pour une région spécifique. Certains titres peuvent être lus dans une seule région, certains peuvent être joués dans plusieurs régions, tandis que d’autres peuvent être joués dans toutes les régions. Les régions 1 à 6 ont été définies dans la spécification d’origine du DVD-Video. La région 7 n’est pas définie actuellement. La région 8 a été ajoutée dans 1999 pour des lieux spéciaux, tels que les avions. Les disques DVD-ROM (ceux sans zone vidéo) ne doivent pas contenir de code de région.
-   Lecteur de DVD-ROM. Il existe deux types de lecteurs de DVD-ROM : les lecteurs RPC phase 1 (RPC1) et les lecteurs RPC phase 2 (RPC2). Les lecteurs RPC1 n’ont pas de prise en charge matérielle intégrée pour la gestion des régions. Pour ces lecteurs, Windows gère les informations sur le nombre de modifications de la région et la région ne peut être modifiée qu’une seule fois. Les lecteurs RPC2 maintiennent les informations sur le nombre de modifications de région dans le matériel et en général, la région de ces lecteurs peut être modifiée jusqu’à 5 fois.
-   Décodeur DVD. Certains décodeurs DVD, matériel ou logiciel, sont définis pour une région spécifique. En général, l’utilisateur ne peut pas modifier la région du décodeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge des modifications de région de DVD dans Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



