---
description: Améliorations futures de l’exemple de code d’application Winsock.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Améliorations futures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008278"
---
# <a name="future-improvements"></a>Améliorations futures

Plusieurs améliorations peuvent être apportées à cette application, par exemple :

-   Une seule connexion permanente peut être créée par l’application. La gestion des erreurs appropriée devrait être ajoutée. Cela réduirait la surcharge associée au démarrage et à la destruction de la connexion.
-   Le code de réponse sur le serveur peut être optimisé pour consolider les réponses, ce qui réduit le nombre de paquets envoyés à partir du serveur.
-   Des améliorations ont été apportées au protocole. Par exemple, un masque de mise à jour peut être utilisé pour indiquer les cellules à mettre à jour et uniquement les données de cette cellule envoyées.
-   Les mises à jour peuvent être superposées à l’aide de différents threads, afin que le réseau ne soit pas inactif pendant l’exécution de la fonction **ComputeNext** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Amélioration d’une application lente](improving-a-slow-application-2.md)
</dt> <dt>

[Version de référence : une application très médiocre](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Révision 1 : nettoyage évident](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Révision 2 : reconception pour des connexions moins nombreuses](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Révision 3 : envoi de bloc compressé](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



