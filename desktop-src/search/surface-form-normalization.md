---
description: Bien que les mots et les règles linguistiques diffèrent considérablement, certaines considérations, telles que les nombres, les dates et les heures, sont gérées de manière cohérente sur tous les analyseurs lexicaux.
ms.assetid: 62545566-f0ba-4876-93da-e6c2b9c23484
title: Normalisation des formes de surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f96ce5c90075c49608ad386b64514e4d003e5b5b4c6fc582441fd7e110d1921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862433"
---
# <a name="surface-form-normalization"></a>Normalisation des formes de surface

Bien que les mots et les règles linguistiques diffèrent considérablement, certaines considérations, telles que les nombres, les dates et les heures, sont gérées de manière cohérente sur tous les analyseurs lexicaux. Cette rubrique décrit les considérations relatives à la normalisation qui peuvent affecter votre implémentation de l’analyseur lexical.

Cette rubrique est organisée comme suit :

-   [Coupure](#hyphenation)
-   [Possessifs](#possessives)
-   [Signes diacritiques](#diacritics)
-   [Clitics](#clitics)

## <a name="hyphenation"></a>Coupure

Les traits d’Union (-) sont utilisés entre les parties d’un mot ou d’un nom composé. Elles sont également utilisées entre les syllabes d’un mot lorsque le mot est divisé à la fin d’une ligne de texte. En anglais, les mots sont joints par des traits d’Union pour indiquer une relation spéciale en contexte, mais ces mots ne peuvent normalement pas être coupés dans d’autres contextes. par exemple, « pas à pas ». Pendant la création de l’index, l’analyseur lexical doit traiter le trait d’Union comme un séparateur de mots. Par exemple, « Data-base » est stocké en tant que « Data » plus « base ». Au moment de la requête, une expression de découpage doit être remplacée par deux alternatives : la variante à deux mots et le vrai. Par exemple, « Data-base » est remplacé par « Data » plus « base » et « base de données ». Cette différence entre l’index et le temps de requête augmente les combinaisons de représentations pour les mots avec trait d’Union et rend les mots plus faciles à faire correspondre dans une requête.

Le tableau suivant montre comment le traitement des traits d’Union en tant que séparateurs de mots dans la langue anglaise augmente le nombre de termes de requête correspondants pour chaque terme inclus dans l’index.



| Termes inclus dans l’index | Correspondances au moment de la requête   |
|-----------------------------|----------------------|
| Base de données                   | base de données, base de données |
| Base de données                   | base de données, base de données |
| Base de données                    | base de données, base de données  |



 

## <a name="possessives"></a>Possessifs

Les possessifs sont des variations d’un nom qui indiquent possession. Les possessifs en anglais sont représentés par l’ajout d’une apostrophe (') ou d’une apostrophe et d’un (e) à un mot. Par exemple, pour indiquer possession, le mot « Mary » est représenté par « Mary ». L’analyseur lexical génère l’apostrophe et les formes apostrophes au moment de la requête. Les requêtes pour « Mary » doivent correspondre à la fois à « Mary » et à « Mary ».

## <a name="diacritics"></a>Diacritiques

Les signes diacritiques sont des marques ajoutées à une lettre ou au phonème pour indiquer une valeur phonétique spéciale pour la prononciation. Les signes diacritiques peuvent distinguer les mots qui sont autrement sous une forme graphique identique ; par exemple, « Resume » et « Resumé » en anglais. Toutefois, l’enregistrement de signes diacritiques dans l’index augmente le nombre de clés de mot uniques dans l’index, ce qui ralentit les performances des requêtes. Si les signes diacritiques sont utilisés au minimum dans une langue, l’analyseur lexical pour cette langue doit les supprimer lors de la création et de l’interrogation d’index. Par exemple, l’analyseur lexical anglais génère la « reprise » lors du traitement de « Resumé », ce qui n’a qu’un impact minime sur la pertinence des résultats de la requête.

## <a name="clitics"></a>Clitics

Un clitic est un mot sans contrainte qui n’est pas capable de se reposer seul et qui s’attache à un mot trop sollicité pour former une seule unité. Clitics ne peut pas être facilement classé comme Phonological, syntaxique ou morphologique. Les clitics sont de deux types : *proclitics* et *enclitics*. Proclitics s’attache au début d’un mot. Enclitics s’attache à la fin d’un mot.

Les clitics sont plus difficiles à analyser dans des langages tels que l’espagnol. Un verbe espagnol peut générer de nombreuses formes superficielles, en fonction du temps. Il convient de tenir compte de la suppression des clitic lors de la création d’index et de la génération des formes de surface via la recherche de radical au moment de la requête. La suppression de clitics dans les cas où la morphologie de la composition clitic est ambiguë peut entraîner des résultats imprévisibles. La génération d’un grand nombre de formes de surface pour un mot augmente la taille de l’index de recherche en texte intégral et peut ralentir les performances des requêtes. Il est recommandé que le générateur de formes dérivées ne génère qu’un petit nombre de formes de surface.

 

 



