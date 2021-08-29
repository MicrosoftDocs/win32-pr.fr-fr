---
description: Lorsqu’une opération de sauvegarde VSS est effectuée sans implication d’un enregistreur, la création de clichés instantanés peut encore se produire.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Sauvegardes sans participation au rédacteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bd1d402b53c48fd82085110e4d58600c92fbdd72defc47dee326c8fa1d4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248279"
---
# <a name="backups-without-writer-participation"></a>Sauvegardes sans participation au rédacteur

Lorsqu’une opération de sauvegarde VSS est effectuée sans implication d’un enregistreur, la création de clichés instantanés peut encore se produire.

Comme indiqué ailleurs (voir [État de cliché instantané par défaut](shadow-copies-and-shadow-copy-sets.md)), le résultat de ce type de cliché instantané est un volume qui reflète l’état d’un disque au moment du cliché instantané : les données sur le volume copié par cliché instantané peuvent refléter des opérations d’e/s incomplètes ou partielles et sont décrites comme étant dans un [*État de cohérence*](vssgloss-c.md)en cas d’incident.

Il existe plusieurs situations qui nécessitent une application de sauvegarde pour fonctionner avec des données de clichés instantanés cohérentes en cas d’incident :

-   **Les données sont gérées par des applications qui ne prennent pas en charge VSS**

    Presque tous les systèmes disposent de certaines applications, telles que les éditeurs de texte, les lecteurs de messagerie, les traitements de texte, etc., qui ne sont pas compatibles avec VSS. il est donc toujours probable que certaines des données d’un cliché instantané devront être considérées comme étant dans un état de cohérence d’incident.

    Ce type de données n’étant généralement pas critique dans le système ou le service, la sauvegarde ne doit pas être problématique, ou au moins plus problématiques que lors d’une sauvegarde conventionnelle.

    Comme avec les préparations pour les sauvegardes conventionnelles, si possible, les opérateurs de sauvegarde doivent tenter d’interrompre ou de mettre fin à ces applications avant de démarrer un travail de sauvegarde VSS.

-   **Système sans Writers compatibles VSS**

    cette situation peut être relativement rare, car la plupart des systèmes qui peuvent être sauvegardés par une application de sauvegarde vss auront une version vss de Windows, qui doit contenir des enregistreurs.

    Toutefois, dans certains cas, ce problème peut survenir : par exemple, si vous sauvegardez un système sans la prise en charge de VSS, mais que le système utilise une appliance en réseau compatible VSS pour son stockage.

    Bien que la sauvegarde de l’état d’un système à partir d’une image cohérente en cas d’incident ne soit pas optimale, il peut suffire qu’un ordinateur redémarre à un état opérationnel. Dans de nombreux cas, l’ordinateur récupère les opérations d’e/s incomplètes dans les systèmes de fichiers et fonctionne normalement.

-   **Un demandeur choisit de ne pas travailler avec les enregistreurs système**

    Cette situation se produit si un demandeur a choisi d’ajouter des composants d’écriture ou de désactiver tous les enregistreurs.

    L’exécution de sauvegardes de cette manière est généralement déconseillée. Bien que le volume cliché instantané à sauvegarder puisse être suffisant pour restaurer un système en cours d’exécution, il n’est pas souhaitable. En fait, étant donné que les writers qui s’exécutent sur le système sont conçus avec des fonctionnalités permettant de coopérer avec VSS et les clichés instantanés, la sauvegarde de leurs données de cette manière peut entraîner une instabilité.

 

 



