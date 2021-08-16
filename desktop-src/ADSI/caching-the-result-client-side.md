---
title: Mise en cache du résultat (côté client)
description: La mise en cache côté client stocke le jeu de résultats dans la mémoire du client, ce qui permet d’améliorer les performances côté client.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Mise en cache du résultat (côté client) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2394c4f9e3213261bc52e15ada6fa9416703706fedeccaf144493821133e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840499"
---
# <a name="caching-the-result-client-side"></a>Mise en cache du résultat (côté client)

La mise en cache côté client stocke le jeu de résultats dans la mémoire du client, ce qui permet d’améliorer les performances côté client. Un client peut réexaminer un objet de façon répétée sans plusieurs allers-retours au serveur. Par défaut, ADSI met en cache le jeu de résultats pour les clients. cela permet à ADSI de fournir aux clients une prise en charge des curseurs de type SQL. Vous pouvez effectuer une itération à travers un jeu de résultats donné plusieurs fois.

ADSI permet également aux clients de désactiver le cache pour réduire les besoins en mémoire. Si la mise en cache côté client est désactivée, le client ne conserve pas le jeu de résultats en mémoire. Chaque ligne est libérée une fois que l’application l’a récupérée. La désactivation de la mise en cache côté client peut être utile pour réduire les besoins en mémoire côté client dans ce cas, comme lorsque vous envisagez de faire une seule passe dans le jeu de résultats. Toutefois, lorsque les clients choisissent de ne pas mettre en cache le résultat, ils accèdent à la prise en charge des curseurs.

Pour plus d’informations sur la mise en cache des résultats avec une interface de recherche spécifique, consultez :

-   [Mise en cache des résultats avec IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




