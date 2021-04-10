---
description: Recommandations pour les transactions de système de fichiers optimales.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Considérations relatives aux performances pour le NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a71f7e100e1ddd8524932a4a259a12092bddcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952642"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Considérations relatives aux performances pour le NTFS transactionnel

Le NTFS transactionnel (TxF) a été soigneusement conçu pour les performances et est généralement plus performant que les alternatives transactionnelles à usage général dans des scénarios similaires. Toutefois, les transactions de système de fichiers ont plus de charge que les opérations non transactionnelles et une réduction des performances d’e/s par rapport aux e/s non transactionnelles est attendue. Les applications critiques pour les performances doivent effectuer un cycle de qualification d’adoption de technologie, en évaluant l’impact sur les performances des opérations de système de fichiers transactionnelles.

## <a name="overview-of-txf-operations"></a>Vue d’ensemble des opérations TxF

TxF utilise la journalisation des *annulations* pour enregistrer les modifications nécessaires pour réintégrer le système de fichiers dans un état cohérent, également appelé restauration, en cas d’abandon d’une transaction. Cette annulation de journalisation génère des e/s supplémentaires et constitue la source de la surcharge de performances TxF par rapport aux opérations de système de fichiers non transactionnelles.

Voici une synthèse générale du fonctionnement de TxF :

-   À mesure qu’une transaction progresse, TxF écrit des enregistrements d' *annulation* dans son fichier journal pour chaque modification qu’il effectue dans le système de fichiers. En cas d’abandon, ces enregistrements d’annulation sont analysés pour replacer le système de fichiers dans l’État où il se trouvait avant le début de la transaction.
-   Un enregistrement d’annulation de *modification de métadonnées* décrit une modification apportée uniquement aux métadonnées du système de fichiers. Le déplacement, le changement de nom, les ajouts et les modifications d’attributs sont des exemples. Pour les enregistrements d’annulation de modification de métadonnées, toutes les informations nécessaires pour annuler la modification se trouvent dans l’enregistrement et stockées dans le fichier journal.
-   Un enregistrement d’annulation de *remplacement* décrit un remplacement d’une partie d’un fichier. Lorsqu’un remplacement de fichier se produit, le contenu d’origine du fichier est stocké dans un fichier d’annulation spécial dans un répertoire masqué et l’enregistrement d’annulation du remplacement pointe sur ce fichier. Lorsque des mises à jour de fichiers sont finalement vidées du cache au disque, le contenu du fichier d’annulation doit également être vidé. par conséquent, un remplacement de fichier transactionnel peut générer jusqu’à deux opérations d’e/s aléatoires supplémentaires : une pour lire les anciennes données et une pour les écrire dans le fichier d’annulation. Ces opérations d’e/s supplémentaires sont un coût de fonctionnement de TxF.
-   Lorsqu’une validation se produit, TxF vide tout d’abord toutes les informations d’annulation, puis vide les modifications de fichier réelles, puis écrit et vide un enregistrement de validation. S’il n’y a aucun fichier d’annulation à vider, la seule surcharge TxF supplémentaire relative aux e/s non transactionnelles est le vidage des journaux. Toutefois, les vidages du journal entraînent des écritures séquentielles volumineuses efficaces, ce qui réduit le coût des performances.
-   TxF est optimisé pour la validation. Il est prévu que la plupart des transactions aboutissent et n’aient pas besoin d’être restaurées. par conséquent, tous les enregistrements d’annulation d’une transaction sont censés être inutilisés. Du point de vue des performances, les opérations de validation TxF sont rapides et les restaurations nécessitent beaucoup de ressources.
-   La restauration est plus gourmande en ressources que la validation. Pendant la restauration, toutes les modifications apportées à la transaction doivent être annulées. En général, la durée de la restauration peut être approximativement la même que celle qui a été nécessaire pour apporter les modifications à l’origine. Par exemple, s’il a fallu 1 seconde pour effectuer toutes les modifications, il peut prendre environ 1 seconde pour les annuler. Pour les transactions très longues, la restauration peut créer des impacts supplémentaires sur les performances. Par exemple, le temps de démarrage du système peut être retardé si le système doit restaurer automatiquement une transaction dans le cas où le système cesse de répondre et doit effectuer un redémarrage non planifié.

Les conclusions résumées concernant les performances qui peuvent être extraites de la liste précédente sont les suivantes :

-   Le coût des performances de TxF pour les transactions impliquant des remplacements de fichiers peut être significatif.
-   Le coût des performances de TxF pour les transactions impliquant uniquement des opérations de métadonnées peut être relativement faible, à condition que des transactions volumineuses soient utilisées. Une transaction importante est lorsqu’il existe de nombreux enregistrements d’annulation pour chaque enregistrement de validation.

## <a name="recommendations-for-best-performance"></a>Recommandations pour des performances optimales

Amortir la surcharge TxF sur des transactions plus volumineuses. Par exemple, si vous avez *n* ensembles de modifications à faire lorsque chaque modification comporte *m* étapes et que vous avez la possibilité de le faire comme *n* transactions de *m* étapes, chacune d’entre elles, ou de la faire comme une seule transaction avec *m* \* *N* étapes, cette dernière option est plus efficace.

Tenez compte de l’impact possible sur le démarrage des transactions très volumineuses. Comme indiqué précédemment, la restauration peut être lente et retarder le démarrage si le système doit effectuer des restaurations automatiques au moment du démarrage. Plus la transaction est grande, plus le délai est long.

Conservez les transactions dans la plupart des opérations de métadonnées. C’est ce que TxF est optimisé pour et, en général, les performances sont identiques à celles des e/s de fichier non transactionnelles pour les transactions de métadonnées volumineuses. [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda), [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda), [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda), [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda), [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)et les écritures ajoutées (appels à la fonction [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) lorsque le pointeur de fichier se trouve à la fin du fichier ou *EOF*) sont des exemples de fonctions de métadonnées efficaces. Un exemple d’opérations non-métadonnées consommatrices de ressources sont des appels à la fonction **WriteFile** lorsque le pointeur de fichier n’est pas au EOF.

## <a name="summary-of-txf-performance-expectations"></a>Résumé des attentes de performances TxF

Pour les mises à jour sur place, les remplacements dans une section d’un fichier sont beaucoup plus lents que les e/s de fichier non transactionnelles, tandis que les performances TxF pour les opérations de métadonnées du système de fichiers (par exemple, Create, Move et Append) sont comparables aux e/s de fichier non transactionnelles pour les transactions volumineuses.

 

 



