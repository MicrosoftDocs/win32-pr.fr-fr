---
description: L’attribut de transaction est une propriété déclarative qui gère automatiquement les transactions pour le développeur de composants. En définissant cet attribut, vous éliminez le besoin d’utiliser des contrôles de transaction explicites dans votre composant.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Configuration des transactions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d613eb49a5f053b869e3efc90e04b9455644ea52acbaf651f33b00909e6e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128885"
---
# <a name="configuring-transactions"></a>Configuration des transactions

L' *attribut de transaction* est une propriété déclarative qui gère automatiquement les transactions pour le développeur de composants. En définissant cet attribut, vous éliminez le besoin d’utiliser des contrôles de transaction explicites dans votre composant.

COM+ utilise l’attribut de transaction du composant pour déterminer le type de protection de transaction requis pour chaque objet qu’il active. En fonction de ses besoins, un objet peut partager la transaction de son appelant, exiger une nouvelle transaction ou fonctionner sans protection des transactions.

COM+ fournit les valeurs d’attribut de transaction suivantes :

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Activée
</dt> <dd>

En général, vous devez définir cette valeur d’attribut uniquement lorsque vous êtes sûr que le composant n’accède jamais à un gestionnaire de ressources. Lorsque vous désactivez l’attribut de transaction, COM+ ignore les exigences transactionnelles du composant pour déterminer l’emplacement du contexte de l’objet. Par conséquent, l’objet peut partager le contexte de son appelant (et la transaction). Lors de la migration d’un composant COM vers COM+, vous devez désactiver l’attribut transaction pour conserver le même comportement transactionnel que le composant COM non configuré.

> [!Note]  
> Un *composant non configuré* est un composant COM qui n’a pas été installé dans une application com+.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Non pris en charge
</dt> <dd>

Lorsque vous définissez cette valeur d’attribut, COM+ garantit que tous les objets créés à partir du composant ne participent jamais à une transaction, quel que soit l’état transactionnel de son appelant. En déclarant cette valeur, vous vous assurez qu’un objet ne vote pas dans la transaction de son appelant et ne peut pas commencer une transaction qui lui est propre. Non pris en charge est la valeur par défaut pour tous les composants.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Géré
</dt> <dd>

Lorsque vous définissez cette valeur d’attribut, COM+ garantit que tous les objets créés à partir du composant participent à une transaction, le cas échéant. Vous pouvez déclarer cette valeur lorsque vous souhaitez qu’un objet soit partagé dans la transaction de son appelant sans qu’il soit nécessaire de disposer d’une transaction propre.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Obligatoire
</dt> <dd>

Lorsque vous définissez cette valeur d’attribut, COM+ garantit que tous les objets créés à partir du composant sont transactionnels. Lorsque COM+ active un objet avec le paramètre requis, il examine l’état transactionnel de son appelant. Si l’appelant a une transaction, le nouvel objet est inclus dans la transaction en cours. Dans le cas contraire, COM+ commence une transaction, en faisant du nouvel objet la racine de la transaction. Il s’agit du paramètre par défaut pour un composant qui exécute des activités de ressources, car il permet de fournir une protection des transactions pour ces activités.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Nouvelles
</dt> <dd>

Lorsque vous définissez cette valeur d’attribut, COM+ garantit que tous les objets créés à partir du composant doivent participer à une nouvelle transaction comme racine de la transaction, quel que soit l’état transactionnel de l’appelant. COM+ lance automatiquement une nouvelle transaction qui est distincte de la transaction de l’appelant.

> [!Note]  
> COM+ ne prend pas en charge les transactions imbriquées. Lorsqu’un objet transactionnel appelle un autre composant marqué comme nécessite New, COM+ crée une limite transactionnelle indépendante pour l’objet qui vient d’être activé. La deuxième transaction ne peut pas affecter la première transaction, sauf si la première transaction note explicitement les résultats de la deuxième transaction et modifie son vote en fonction de ces résultats.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Dépendances d’attribut de transaction

Le tableau suivant présente les caractéristiques de chaque valeur d’attribut de transaction COM+, y compris l’effet de la valeur sur les caractéristiques de transaction. COM+ applique [l’activation](com--just-in-time-activation.md) et la [synchronisation](com--synchronization.md) JIT pour tous les composants de transaction.



| Valeur d'attribut          | Nouvelle transaction   | Transaction du client                 | Racine de la transaction                        | Activation juste-à-temps      | Synchronisation     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Désactivé<br/>      | Jamais<br/>  | Peut-être<br/>                     | Jamais<br/>                        | Facultatif<br/> | Facultatif<br/> |
| Non pris en charge<br/> | Jamais<br/>  | Jamais<br/>                     | Jamais<br/>                        | Facultatif<br/> | Facultatif<br/> |
| Pris en charge<br/>     | Jamais<br/>  | Si le client a une transaction<br/> | Jamais<br/>                        | Obligatoire<br/> | Obligatoire<br/> |
| Obligatoire<br/>      | Peut-être<br/>  | Si le client a une transaction<br/> | Si le client n’a pas de transaction<br/> | Obligatoire<br/> | Obligatoire<br/> |
| Nouveau requis<br/>  | Toujours<br/> | Jamais<br/>                     | Toujours<br/>                       | Obligatoire<br/> | Obligatoire<br/> |



 

## <a name="transaction-boundaries"></a>Limites de transaction

Une transaction a un début, une fin et se produit exactement une fois. Pendant son exécution, une transaction peut appeler sur une ressource, telle qu’une base de données ou une file d’attente, pour accomplir une ou plusieurs tâches. Chaque ressource est comprise dans la limite de la *transaction*. Toutes les ressources au sein d’une limite de transaction, qui peuvent s’étendre sur plusieurs limites de processus et d’ordinateur, partagent une seule transaction. La gestion de la cohérence entre ces processus et les limites de l’ordinateur est importante.

COM+ garantit la cohérence en gérant automatiquement les limites de transaction, en fonction de la valeur de l’attribut de transaction que vous avez défini pour chaque composant. Une transaction COM+ est automatiquement transférée aux objets qui doivent participer à une transaction et ignore les objets qui doivent être exécutés en dehors d’une transaction. COM+ ne prend pas en charge les transactions imbriquées. Au lieu de cela, les transactions COM+ sont distinctes et éphémères.

Le premier objet dans une limite de transaction est spécial pour la transaction et est appelé l' *objet racine* de la transaction. Il ne peut y avoir qu’un seul objet racine dans une transaction. Tous les autres objets de la hiérarchie transactionnelle sous l’objet racine sont appelés *objets intérieurs*.

## <a name="mapping-transactions"></a>Mappage de transactions

Une façon de s’assurer qu’un objet est inclus dans la limite de transaction correcte consiste à mapper vos transactions avant de commencer à écrire vos composants. En mappant les transactions, vous pouvez déterminer le meilleur paramètre pour chaque composant que vous écrivez. Plus vous êtes certain de l’utilisation de vos composants, plus il est facile de sélectionner la valeur d’attribut de transaction correcte.

Au moment de l’exécution, COM+ examine l’attribut de transaction pour déterminer si un objet doit être la racine d’une nouvelle transaction, être créé dans une transaction existante ou être créé en tant qu’objet non transactionnel.

L’illustration suivante montre un mappage de transaction possible. Dans l’illustration, le client crée l’objet 1, qui requiert une transaction. Étant donné qu’il n’existe aucune transaction, COM+ crée la transaction 1 et place l’objet 1 dans celui-ci en tant qu’objet racine. Object 1 crée l’objet 2, qui prend en charge les transactions et est donc placé dans la transaction 1. L’objet 2 crée l’objet 3, qui ne prend pas en charge les transactions et est donc placé en dehors de toutes les transactions. L’objet 2 crée également l’objet 4, qui requiert une transaction et est donc placé dans la transaction 1. L’objet 3 crée l’objet 5, qui prend en charge les transactions. Toutefois, étant donné que l’objet 5 est créé par un objet qui n’existe pas dans une transaction, il est également placé en dehors de toutes les transactions. L’objet 4 crée l’objet 6, qui nécessite une nouvelle transaction, de sorte que COM+ crée la transaction 2 et place l’objet 6 en tant qu’objet racine. L’objet 6 crée l’objet 7, qui prend en charge les transactions et est donc placé dans la transaction 2.

![Diagramme illustrant une interaction client avec la transaction 1 et la transaction 2.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

L’illustration précédente montre deux problèmes potentiels. Tout d’abord, la majorité du travail est divisée entre deux transactions distinctes. Si la transaction 1 échoue après que l’objet 4 a créé l’objet 6, la transaction 2 n’est pas affectée par le résultat de la transaction 1. Si ce résultat n’est pas intentionnel, vous préférerez peut-être plier les opérations des deux transactions en une seule transaction, ce que vous pouvez effectuer en remplaçant l’attribut de transaction de l’objet 6 par requis.

L’illustration de mappage indique également que les objets 3 et 5 sont non transactionnels, qui s’exécutent complètement en dehors de l’étendue des transactions 1 et 2. Si l’objet 5 met à jour les données persistantes, vous souhaiterez peut-être reconsidérer son état non transactionnel. L’objet 5 peut être placé dans une transaction en remplaçant son attribut de transaction par required.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de l’attribut de transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




