---
description: La valeur de retour des fonctions PDH indique la réussite ou l’échec de l’appel de fonction, qui est différent de l’état des données de compteur.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Vérification des codes d’état des données de compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7daed51ba6e8df385170b9a23b419267409ef497
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013903"
---
# <a name="checking-counter-data-status-codes"></a>Vérification des codes d’état des données de compteur

La valeur de retour des fonctions PDH indique la réussite ou l’échec de l’appel de fonction, qui est différent de l’état des données de compteur. Vérifiez toujours le membre **CStatus** d’une valeur de compteur retournée dans les structures PDH pour vous assurer que les données retournées sont valides avant de l’utiliser. Si la valeur du membre **CStatus** n’indique pas de réussite, n’utilisez pas les données. Les valeurs d’État possibles pour les compteurs sont les suivantes :



| Valeur                              | Signification                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ aucun \_ ordinateur          | PDH n’a pas pu se connecter à l’ordinateur spécifié dans le chemin d’accès au compteur. Si cet État est retourné lorsque le compteur est ajouté, le compteur n’est pas complètement initialisé. Chaque fois que la requête est mise à jour, PDH effectue une nouvelle tentative de connexion. Lorsque la connexion est établie, la collecte de données normale reprend.                                                                  |
| PDH \_ CSTATUS \_ aucun \_ objet           | L’ordinateur spécifié a été trouvé, mais l’objet de performance spécifié a été trouvé sur l’ordinateur. Si cet État est retourné lorsque le compteur est ajouté, le compteur spécifié n’est pas inclus dans la requête. Si cet État est retourné par un compteur actif, les données de ce compteur ne sont pas valides. Chaque fois que les données sont demandées, PDH tente d’obtenir ces données de compteur. |
| PDH \_ CSTATUS \_ aucune \_ instance         | L’instance spécifiée est introuvable dans l’objet. Si cet État est retourné lorsque le compteur est ajouté à la requête, le compteur est correctement ajouté à la requête, mais aucune donnée n’est disponible tant que l’instance spécifique n’apparaît pas et qu’un état de réussite n’est pas retourné.                                                                                                  |
| PDH \_ CSTATUS \_ aucun \_ compteur          | Le compteur spécifié est introuvable dans l’objet spécifié. Si cet État est renvoyé lorsque le compteur est ajouté, le compteur n’est pas ajouté à la requête. Si cet État est retourné après la collecte de données, les données de ce compteur ne sont pas valides. Chaque fois que les données sont demandées, PDH tente d’obtenir ces données de compteur.                                             |
| PDH \_ CSTATUS \_ données non valides \_        | Le compteur a été trouvé, mais les données retournées ne sont pas valides. Cette erreur peut se produire si la valeur de compteur est inférieure à la valeur précédente. (Étant donné que les valeurs de compteur sont toujours incrémentées, la valeur de compteur passe à zéro lorsqu’elle atteint sa valeur maximale.) Une autre cause possible est une horloge système qui n’est pas correcte.                                              |
| PDH \_ CSTATUS \_ données valides \_          | Les données du compteur ont été retournées, mais elles ne sont pas modifiées à partir de la dernière lecture du compteur.                                                                                                                                                                                                                                                                    |
| PDH \_ CSTATUS \_ nouvelles \_ données            | Les données du compteur ont été retournées avec succès et diffère de la dernière fois que le compteur a été lu. PDH \_ CSTATUS les \_ nouvelles \_ données peuvent être retournées sur un compteur de taux même si le taux résultant est le même que celui du dernier échantillon. Cela est dû au fait que la valeur de données brutes utilisée dans la détermination de cette valeur d’État a changé, et non le taux calculé.                  |
| PDH \_ \_ données supplémentaires                    | La mémoire tampon fournie n’était pas assez grande pour stocker toutes les données de compteur. Allouez une mémoire tampon plus grande et réexécutez la fonction.                                                                                                                                                                                                                                              |
| \_élément CSTATUS \_ PDH \_ non \_ validé | Le compteur a été ajouté à la requête, mais n’a pas été validé ni accédé. Aucune information d’État supplémentaire n’est disponible sur ce compteur.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ no \_ COUNTERNAME      | Aucun nom de compteur n’a été spécifié dans la requête.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CSTATUS \_ aucun \_ compteur          | Le nom de compteur spécifié est introuvable.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ aucun \_ objet           | L’objet de performance spécifié est introuvable.                                                                                                                                                                                                                                                                                                                             |
| PDH \_ Calc \_ - \_ dénominateur négatif   | Un compteur a une valeur de dénominateur négative.                                                                                                                                                                                                                                                                                                                                      |
| valeur du temps de \_ calcul négatif du calcul PDH \_ \_      | Un compteur a une valeur de la porte de temps négative.                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ valeur négative du calcul PDH \_         | Un compteur a une valeur négative.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ no \_ COUNTERNAME      | Aucun chemin de compteur n’a été spécifié.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ , \_ COUNTERNAME incorrect     | Le format du chemin d’accès au compteur est incorrect.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



