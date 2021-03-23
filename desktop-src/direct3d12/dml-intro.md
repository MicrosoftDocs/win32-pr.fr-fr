---
title: Introduction à DirectML
description: Direct Machine Learning (DirectML) est une API de bas niveau pour Machine Learning (ML).
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 2dd37bc4c27364e26e4bbd4ae2cf5d43031c3314
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104220"
---
# <a name="introduction-to-directml"></a>Introduction à DirectML

## <a name="summary"></a>Résumé

Direct Machine Learning (DirectML) est une API de bas niveau pour Machine Learning (ML). Les primitives Machine Learning accélérées par le matériel (appelés opérateurs) sont les blocs de construction de DirectML. À partir de ces blocs de construction, vous pouvez développer des techniques de Machine Learning telles que la mise à l’échelle, l’anticrénelage et le transfert de style, à un nom donné. Denoising et la Super-résolution, par exemple, vous permettent d’obtenir des effets raytraced impressionnants avec moins de rayons par pixel.

Vous pouvez intégrer l’apprentissage machine par le biais d’inférences de charges de travail dans votre jeu, votre moteur, votre intergiciel (middleware), votre serveur principal ou toute autre application. DirectML dispose d’une interface de programmation de style et d’un flux de travail DirectX 12 familiers (C++ natif, nano-COM) et est prise en charge par tous les matériels compatibles DirectX 12. Pour obtenir des exemples d’applications DirectML, y compris un exemple d’application DirectML minimale, consultez [exemples d’applications DirectML](dml-min-app.md).

DirectML est introduit dans Windows 10, version 1903 et dans la version correspondante du SDK Windows.

## <a name="is-directml-appropriate-for-my-project"></a>Le DirectML est-il adapté à mon projet ?

DirectML est un composant de l’parapluie [Windows machine learning](/windows/ai) . L’API WinML de niveau supérieur est principalement axée sur les modèles, avec son flux de travail de liaison de charge et d’évaluation. Toutefois, les domaines tels que les jeux et les moteurs nécessitent généralement un niveau d’abstraction inférieur et un degré de contrôle du développeur plus élevé, afin de tirer pleinement parti du silicium. Si vous comptez des millisecondes et des temps de compression, DirectML répond à vos besoins en matière de Machine Learning.

Pour des scénarios fiables, en temps réel et à faible latence, et/ou à ressources restreintes, utilisez DirectML (plutôt que WinML). Vous pouvez intégrer DirectML directement dans le moteur ou le pipeline de rendu existant. Ou, à un niveau plus élevé pour les infrastructures d’Machine Learning personnalisées et les intergiciel, DirectML peut fournir un backend haute performance sur Windows.

WinML est lui-même implémenté à l’aide de DirectML comme l’un de ses serveurs principaux.

## <a name="what-work-does-directml-do-and-what-work-must-i-do-as-the-developer"></a>Ce que fait DirectML le travail ; et quel travail dois- *je* faire en tant que développeur ?

DirectML exécute efficacement les couches individuelles de votre modèle d’inférence sur le GPU (ou sur les cœurs d’accélération AI, le cas échéant). Chaque couche est un opérateur et DirectML vous fournit une bibliothèque d’opérateurs de niveau inférieur, accéléré par le matériel Machine Learning. Ces opérateurs ont des optimisations propres au matériel et à l’architecture, qui sont conçues pour eux ( [nous en ReDirectMLnt](#why-does-directml-perform-so-well)davantage dans la section pourquoi les performances sont-elles tellement bonnes ?). En même temps, en tant que développeur, vous voyez une interface unique indépendante du fournisseur pour l’exécution de ces opérateurs.

La bibliothèque d’opérateurs dans DirectML fournit toutes les opérations habituelles que vous devriez pouvoir utiliser dans une charge de travail de Machine Learning.

- Les opérateurs d’activation, tels que **Linear**, **ReLU**, **sigmoïde**, **Tanh**, etc.
- Les opérateurs basés sur les éléments, tels que **Add**, **exp**, **log**, **Max**, **min**, **Sub**, etc.
- Les opérateurs de convolution, tels que les **convolutions** 2D et 3D, etc.
- Les opérateurs de réduction, tels que **argmin**, **Average**, **L2**, **Sum**, etc.
- Opérateurs de regroupement, tels que **Average**, **LP** et **Max**.
- Les opérateurs de réseau neuronal (NN), tels que **GEMM**, **Gru**, **LSTM** et **RNN**.
- Et bien plus encore.

Pour des performances maximales, et afin de ne pas payer pour ce que vous n’utilisez pas, DirectML met le contrôle dans vos mains en tant que développeur sur la façon dont votre charge de travail Machine Learning est exécutée sur le matériel. Il vous incombe de déterminer quels opérateurs exécuter et quand, est votre responsabilité en tant que développeur. Les tâches qui sont laissées à votre discrétion incluent : la transcription du modèle ; simplification et optimisation de vos couches ; poids de chargement ; allocation des ressources, liaison, gestion de la mémoire (tout comme avec Direct3D 12); et l’exécution du graphique.

Vous conservez des connaissances de haut niveau de vos graphiques (vous pouvez coder en dur votre modèle directement, ou vous pouvez écrire votre propre chargeur de modèle). Vous pouvez concevoir un **modèle de mise** à l’échelle, par exemple en utilisant plusieurs couches, chacune d’entre elles, les opérateurs de **convolution**, de **normalisation** et d' **activation** . Grâce à cette connaissance, à la planification soignée et à la gestion des barrières, vous pouvez extraire le plus de parallélisme et les performances du matériel. Si vous développez un jeu, votre gestion des ressources minutieuse et le contrôle de la planification vous permettent d’entrelacer Machine Learning charges de travail et le travail de rendu traditionnel afin de saturer le GPU.

## <a name="whats-the-high-level-directml-workflow"></a>Qu’est-ce que le flux de travail DirectML de haut niveau ?

Voici la recette de haut niveau de la façon dont nous pensons que les DirectML sont utilisés. Dans les deux phases principales de l’initialisation et de l’exécution, vous enregistrez votre travail dans des listes de commandes, puis vous les exécutez dans une file d’attente.

### <a name="initialization"></a>Initialisation

1. Créez vos ressources Direct3D 12 sur &mdash; le périphérique Direct3D 12, la file d’attente de commandes, la liste des commandes et les ressources telles que les tas de descripteurs.
2. Étant donné que vous effectuez Machine Learning inférence, ainsi que votre charge de travail de rendu, créez des ressources DirectML &mdash; les instances de l’appareil DirectML et de l’opérateur. Si vous avez un modèle de Machine Learning dans lequel vous devez effectuer un type particulier de convolution avec une taille particulière de tenseur de filtre avec un type de données particulier, alors il s’agit de tous les paramètres de l’opérateur de **convolution** de DirectML.
3. Les enregistrements DirectML fonctionnent dans les listes de commandes Direct3D 12. Ainsi, une fois l’initialisation terminée, vous enregistrez la liaison et l’initialisation de (par exemple) votre opérateur de convolution dans votre liste de commandes. Ensuite, fermez et exécutez votre liste de commandes dans votre file d’attente comme d’habitude.

### <a name="execution"></a>Exécution

1. Chargez vos plus de dizaines de poids dans les ressources. Un tenseur dans DirectML est représenté à l’aide d’une ressource Direct3D 12 standard. Par exemple, si vous souhaitez télécharger vos données de poids vers le GPU, vous procédez de la même façon que vous le feriez avec n’importe quelle autre ressource Direct3D 12 (utilisez un segment de mémoire de chargement ou la file d’attente de copie).
2. Ensuite, vous devez lier ces ressources Direct3D 12 comme des dizaines d’entrée et de sortie. Enregistrement dans votre commande répertorie la liaison et l’exécution de vos opérateurs.
3. Fermez et exécutez votre liste de commandes.

Tout comme avec Direct3D 12, vous êtes responsable de la durée de vie des ressources et de la synchronisation. Par exemple, ne libérez pas vos objets DirectML au moins jusqu’à ce qu’ils aient terminé leur exécution sur le GPU.

## <a name="why-does-directml-perform-so-well"></a>Pourquoi DirectML fonctionne-t-il bien ?

Il y a une bonne raison pour laquelle vous ne devriez pas simplement écrire votre propre opérateur de convolution (par exemple) en langage HLSL dans un [nuanceur de calcul](/windows/desktop/direct3d12/pipelines-and-shaders-with-directx-12#direct3d-12-compute-pipeline). L’avantage de l’utilisation de DirectML est que, en &mdash; dehors de l’économie de l’effort de Homebrewing votre propre solution &mdash; , elle permet de fournir des performances nettement supérieures à celles d’un nuanceur de calcul manuel écrit et à usage général pour une telle **convolution** ou **LSTM**.

DirectML réalise cela en partie en raison de la fonctionnalité de recommandes Direct3D 12. Les recommandes exposent une boîte noire des fonctionnalités jusqu’à DirectML, ce qui permet aux fournisseurs de matériel de fournir un accès DirectML aux optimisations spécifiques au matériel et à l’architecture du fournisseur. Plusieurs opérateurs &mdash; , par exemple, la convolution suivie par l’activation &mdash; peut être regroupé en une seule recommande.  En raison de ces facteurs, DirectML a la possibilité de dépasser les performances d’un nuanceur de calcul à la main, bien écrit et écrit pour s’exécuter sur une large gamme de matériel.

Les recommandes font partie de l’API Direct3D 12, bien qu’elles soient faiblement couplées. Une interface de commande est identifiée par un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)fixe, alors que presque tout le reste sur celle-ci (de son comportement et sa sémantique à sa signature et son nom) ne fait pas strictement partie de l’API Direct3D 12. Au lieu de cela, une commande est spécifiée entre son auteur et le pilote qui l’implémente. Dans ce cas, l’auteur est DirectML. Les « recommandes » sont des primitives Direct3D 12 (comme les dessins et les envois). elles peuvent donc être enregistrées dans une liste de commandes et planifiées pour être exécutées ensemble.

DirectML accélère vos charges de travail Machine Learning à l’aide d’une suite complète de recommandes Machine Learning. Par conséquent, vous n’avez pas besoin d’écrire des chemins de code spécifiques au fournisseur pour obtenir une accélération matérielle pour votre inférence. Si vous exécutez sur une puce d’intelligence artificielle, DirectML utilise ce matériel pour accélérer de manière considérable les opérations telles que la convolution. Vous pouvez utiliser le même code que vous avez écrit, sans le modifier, l’exécuter sur une puce qui n’est pas encore accélérée (par exemple, le GPU intégré de votre ordinateur portable), tout en continuant à bénéficier d’une grande accélération matérielle GPU. Et si aucun GPU n’est disponible, DirectML revient au processeur.
