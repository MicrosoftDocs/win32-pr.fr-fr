---
description: 'La deuxième étape du processus de conception d’une application COM+ consiste à scinder le modèle conceptuel en niveaux logiques de l’architecture à trois niveaux : la couche présentation, ou les services utilisateur. la couche intermédiaire, ou services professionnels ; et la couche données, ou services de données. Si vous n’êtes pas familiarisé avec l’architecture à trois niveaux, consultez Utilisation d’un modèle d’architecture Three-Tier.'
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: 'Modèle logique : définition et planification de l’application'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb09b0d377fcd9bf5e2319868f4006b5dbfce75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111427"
---
# <a name="the-logical-model-application-definition-and-planning"></a>Modèle logique : définition et planification de l’application

La deuxième étape du processus de conception d’une application COM+ consiste à scinder le modèle conceptuel en niveaux logiques de l’architecture à trois niveaux : la *couche présentation*, ou les services utilisateur. la *couche intermédiaire*, ou services professionnels ; et la *couche données*, ou services de données. Si vous n’êtes pas familiarisé avec l’architecture à trois niveaux, consultez [utilisation d’un modèle d’architecture Three-Tier](using-a-three-tier-architecture-model.md).

Commencez ce processus en examinant le modèle conceptuel pour les noms et les verbes. Les noms peuvent souvent se traduire en objets métier (classes), et les verbes qui leur sont associés peuvent être traduits en actions (méthodes des classes). Bien qu’il soit difficile de définir tous les noms comme objets métier, les omissions ou les erreurs deviendront évidentes au moment où vous terminez le modèle logique.

La plupart des objets métier se terminent au niveau des services d’entreprise, avec les objets restants répartis entre les objets d’interface utilisateur dans le niveau des services de l’utilisateur et les objets de données du niveau des services de données. Lorsque vous créez un modèle logique à l’aide de l’architecture à trois niveaux, gardez à l’esprit les points suivants :

-   Certains des noms de la conception conceptuelle ne représentent pas des données physiques réelles, mais peuvent représenter une action sur le système ou sur le rôle d’un objet métier sur le système. Un objet métier peut également être un service qui effectue un certain type de contrôle système, tel qu’un ID de connexion pour la sécurité.
-   Évitez de créer des objets métier vagues en « lisant entre les lignes » dans le [modèle conceptuel](the-conceptual-model--application-requirements.md). Ces objets métier peuvent ne pas être corrects, et vous devez les considérer soigneusement avant de les inclure dans le modèle logique. S’ils sont corrects, ajoutez-les explicitement au modèle conceptuel.
-   Évitez de créer des objets métier qui expriment les mêmes informations ou fonctions ; la duplication peut être coûteuse en termes de vitesse et de performances des applications.
-   Déterminez les dépendances d’objets. Certains noms du modèle conceptuel peuvent simplement être des attributs d’autres objets métier. Déterminez si l’attribut peut exister indépendamment. Si c’est le cas, il doit devenir son propre objet métier. Si ce n’est pas le cas, il doit être associé à l’objet métier approprié.
-   Évitez de créer des objets métier qui tentent de faire trop de choses. La surcharge des objets métier peut signifier plus de temps à séparer le code par la suite et peut constituer un soucis de maintenance. Les objets distincts dans le modèle conceptuel ne doivent pas être combinés ; ils doivent conserver des objets métier distincts. Vous pouvez gérer toutes les similitudes à l’aide du code pour déléguer leurs fonctions courantes à un objet métier.
-   Supprimez tous les objets métier qui ne sont pas utilisés dans les scénarios d’utilisation. Si les objets sont destinés à prendre en compte la croissance future, envisagez de les implémenter une fois l’application initiale terminée.

À ce stade, vous pouvez commencer à penser en termes d’ordinateurs et de code. À partir de ces services professionnels, déterminez les fonctionnalités d’affichage et d’entrée que vous devez fournir en tant que services utilisateur. Définissez les tables et les procédures stockées qui doivent être fournies en tant que services de données. Pour terminer le modèle logique, définissez les interfaces pour chaque service et incluez les définitions de chaque champ de données et leurs règles de validation. Incluez également toutes les fonctions, leur syntaxe et leurs paramètres.

La définition du service ou de l’objet ne doit inclure aucun aspect de l’implémentation physique. L’objectif est de fournir une indication claire pour que les générateurs de composants logiques fonctionnent à partir de et pour permettre à d’autres programmeurs de coder des parties de l’application qui peuvent utiliser le composant avant qu’il ne soit réellement terminé. Dans la conception de modèle logique, vous devez documenter chaque écran, fonction et objet. Ne passez pas au modèle physique ou à l’implémentation tant que vous ne répondez pas à ces critères. Si vous continuez alors que le modèle conceptuel et le modèle logique ne sont pas en accord, vous rencontrerez des problèmes sérieux plus tard dans le cycle de développement.

Le développement incrémentiel d’une application COM+ est courant. Cela implique la création d’un sous-ensemble des composants finaux et connus et leur test via chaque couche de l’application : le client, l’entreprise et les couches de données, par le biais du stockage de données. Ce modèle de travail fournit des informations sur les exigences supplémentaires du client et les considérations relatives à l’implémentation. Ce modèle de travail est souvent testé sur un seul ordinateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle conceptuel : exigences de l’application](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Modèle physique : architecture de l’application](the-physical-model--application-architecture.md)
</dt> <dt>

[Utilisation d’un modèle d’architecture Three-Tier](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



