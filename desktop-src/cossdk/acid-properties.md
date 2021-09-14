---
description: Dans le cas des pionniers du traitement des transactions, l’acronyme ACID est un acronyme atomique, cohérent, isolé et durable.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Propriétés ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013026"
---
# <a name="acid-properties"></a>Propriétés ACID

Dans le cas des pionniers du traitement des transactions, l’acronyme ACID est un acronyme atomique, cohérent, isolé et durable. Pour garantir un comportement prévisible, toutes les transactions doivent posséder ces propriétés de base, ce qui renforce le rôle des transactions stratégiques en tant que propositions « tout ou rien ».

La liste suivante contient une définition et une description de chaque propriété ACID :

<dl> <dt>

<span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomique
</dt> <dd>

Une transaction doit être exécutée une seule fois et doit être atomique : soit la totalité du travail est effectuée, soit aucune d’entre elles n’est. Les opérations au sein d’une transaction partagent généralement une intention commune et sont interdépendantes. En effectuant uniquement un sous-ensemble de ces opérations, le système peut compromettre l’intention globale de la transaction. L’atomicité élimine le risque de traiter uniquement un sous-ensemble d’opérations.

</dd> <dt>

<span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Conforme
</dt> <dd>

Une transaction doit préserver la cohérence des données, transformant un état cohérent des données en un autre État de données cohérent. Une grande partie de la responsabilité du maintien de la cohérence incombe au développeur de l’application.

</dd> <dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Concerné
</dt> <dd>

Une transaction doit être une unité d’isolation, ce qui signifie que les transactions simultanées doivent se comporter comme si chacune était la seule transaction en cours d’exécution dans le système. Étant donné qu’un degré élevé d’isolation peut limiter le nombre de transactions simultanées, certaines applications réduisent le niveau d’isolation dans Exchange pour un meilleur débit. Pour plus d’informations, consultez [Configuration des niveaux d’isolation des transactions](configuring-transaction-isolation-levels.md) .

</dd> <dt>

<span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable
</dt> <dd>

Une transaction doit être récupérable et doit donc avoir une durabilité. Si une transaction est validée, le système garantit que ses mises à jour peuvent être conservées même si l’ordinateur se bloque immédiatement après la validation. La journalisation spécialisée permet à la procédure de redémarrage du système d’effectuer les opérations non terminées requises par la transaction, ce qui rend la transaction durable.

</dd> </dl>

 

 



