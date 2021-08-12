---
description: En règle générale, la latence entre les niveaux d’une application distribuée diffère sensiblement.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Optimisation des interactions entre le niveau de logique métier COM+ et la couche présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca519c6aa7f1585648b0def6530b7f224f12a98961193e4f6f7cc490a747b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306101"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Optimisation des interactions entre le niveau de logique métier COM+ et la couche présentation

En règle générale, la latence entre les niveaux d’une application distribuée diffère sensiblement. Les appels entre le niveau de présentation et le niveau de logique métier sont souvent un ordre de grandeur plus lent que les appels entre le niveau métier et la couche données. Par conséquent, l’État détenu est plus coûteux lors de l’appel au niveau de la logique métier.

Les rubriques suivantes expliquent comment passer des données entre les couches de la présentation et de la logique métier :

-   [Passage de paramètres](#passing-parameters)
-   [Options de passage de données](#data-passing-options)
-   [Utilisation d’un modèle de fabrique pour passer des données](#using-a-factory-pattern-to-pass-data)
-   [Rubriques connexes](#related-topics)

## <a name="passing-parameters"></a>Passage de paramètres

Pour qu’un ensemble d’informations donné soit passé entre la couche de présentation et le niveau de logique métier, vous pouvez avoir une seule ligne, plusieurs lignes ou une combinaison d’une seule ligne (par exemple, un en-tête) et de plusieurs lignes de données de détail. La méthode la plus efficace pour passer ces informations entre les niveaux est un appel de méthode unique. Cet appel unique gère l’ensemble des informations à transmettre. Cela est nécessaire, sauf si vous choisissez de contrôler la transaction à partir de la couche de présentation (et que tout traitement de transaction dans la couche de présentation est identique dans la fonction). Microsoft ne recommande pas de mener des transactions à partir de la couche de présentation, car les appels entre ce niveau et le niveau de logique métier sont généralement les plus lents des appels dans une application multiniveau.

Une façon de créer une telle méthode consiste à passer des lignes d’informations uniques en tant que paramètres et à passer plusieurs lignes en tant que jeux d’enregistrements ADO. Les jeux d’enregistrements sont le cœur de la méthodologie d’accès aux données ADO de Microsoft, et l’utilisation des recordsets ADO vous permet de transmettre toutes les informations relatives à une seule transaction en une seule étape.

## <a name="data-passing-options"></a>Options de passage de données

D’autres options sont à prendre en compte lors du passage de données. Il s’agit notamment de l’utilisation d’une liste de paramètres et d’un jeu d’enregistrements ADO (comme indiqué ci-dessus), de simplement des jeux d’enregistrements ADO, des chaînes encodées XML ou des tableaux de structures. Cette section décrit chacune de ces options.

Le tableau suivant répertorie les zones où des précautions supplémentaires doivent être prises lors de l’utilisation de l’une des quatre possibilités de passage des arguments. Un « X » représente les zones où les compromis doivent être compris et pesés par rapport aux besoins de chaque projet. N’essayez pas de prendre des décisions de passage d’argument pour chaque composant. Les avantages d’un modèle de programmation cohérent dans un projet sont beaucoup plus importants que l’optimisation par méthode ou par composant dans toutes les circonstances sauf les plus extrêmes. Les colonnes sont décrites dans la liste qui suit le tableau.



|     &nbsp;                  | Accès concurrentiel  | WAN          | Déploiement   | Complexité   |
|-----------------------|--------------|--------------|--------------|--------------|
| Entrée | Valeur |
| Recordsets<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Tableaux<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Les quatre colonnes définissent les zones à surveiller lors de l’utilisation de cette option pour passer des paramètres.

-   **La colonne concurrence** représente la nécessité de coder ou de fournir un mécanisme qui gère les conditions de verrouillage sur les opérations de mise à jour. Étant donné que les méthodes qui effectuent des enregistrements peuvent représenter des mises à jour, des problèmes d’accès concurrentiel peuvent survenir. Deux types de verrouillage sont optimistes et pessimistes. Les verrous pessimistes empêchent un utilisateur d’obtenir des données à mettre à jour alors qu’un autre utilisateur est susceptible d’effectuer une mise à jour. Le verrouillage optimiste prend en charge un grand nombre d’utilisateurs en vous permettant de faire face à la probabilité que deux utilisateurs mettent à jour le même document en même temps. Les appels de verrouillage optimistes permettent de vérifier que les données stockées correspondent aux données au moment où une copie des données a été consultée pour modification. Les jeux d’enregistrements ADO assurent la prise en charge automatique du verrouillage optimiste. Les scénarios de mise à jour impliquant des listes de paramètres de lignes uniques ne fournissent pas une prise en charge suffisante pour la vérification de l’accès concurrentiel. XML souffre de ce même problème, dans le cas où aucune reconnaissance du verrouillage n’est présente dans les données XML.
-   **La colonne WAN représente les** conditions dans lesquelles il peut y avoir une contention de transmission sur un réseau étendu (WAN). Lorsque le réseau étendu ne dispose pas d’une capacité suffisante pour gérer l’ensemble des données déplacées à un moment donné, les utilisateurs de l’application rencontrent des retards de temps de réponse. Pour prendre en charge l’accès concurrentiel optimiste, les jeux d’enregistrements ADO déconnectés transmettent deux copies des données du serveur au client. La deuxième copie est utilisée par le client pour déterminer l’ensemble de lignes de mise à jour le plus petit à renvoyer lorsqu’une modification est validée. Bien que cela diminue le trafic du niveau présentation vers les données, la charge supplémentaire de la deuxième copie peut être importante. L’utilisation de recordsets comme seul moyen de transmettre toutes les informations entraîne donc deux fois plus de données qu’il est nécessaire de passer entre les niveaux, sauf lorsque l’ensemble de lignes de mise à jour est renvoyé à la couche de données à partir d’une couche de présentation.
-   **La colonne de déploiement** représente les problèmes associés au passage de données lorsque des technologies spéciales sont requises à la fois sur l’appelant et sur le côté composant du réseau. Par exemple, l’utilisation d’un jeu d’enregistrements ADO requiert que les composants ADO soient présents sur le client et sur le serveur. Les analyseurs XML doivent également être présents des deux côtés, afin d’éviter d’avoir à coder les analyseurs dans vos applications.
-   **La colonne complexité** est indiquée pour les quatre choix, et est une question de préférence ou d’expérience de modèle de programmation antérieure qui peut être déjà établie dans votre organisation de développement. Certaines personnes trouvent que le passage de paramètres est fastidieux et semble qu’elle ajoute trop de complexité au problème de programmation. Le suivi du paramètre que vous gérez et de l’obtention de tous les éléments visibles dans une fenêtre de modification peut créer une complexité logistique que certains développeurs trouvent non gérables.

La méthode de passage de paramètres peut également avoir des compromis, tels que les suivants :

-   Les paramètres peuvent impliquer la gestion de plusieurs arguments et types d’argument, ainsi que le choix du moment approprié pour créer un jeu d’enregistrements à partir d’un paramètre.
-   Les jeux d’enregistrements ADO peuvent réduire les relations hiérarchiques dans les paramètres de méthode jusqu’à un ou deux arguments. Cela simplifie considérablement le modèle de programmation et prend en charge l’ajout de colonnes à un moment ultérieur, mais masque également la hiérarchie d’informations. L’extraction d’informations dans un jeu d’enregistrements ADO et son extraction ultérieure impliquent de connaître le nom de chaque colonne ou de connaître l’ordre des colonnes. Cette situation peut ajouter de la complexité pour d’autres développeurs de composants ou d’applications sur le projet.
-   XML est une fonction différente de la complication de hiérarchie cachée mentionnée ci-dessus. Le programmeur doit comprendre l’utilisation d’un analyseur XML pour accéder aux informations et doit souvent connaître les noms de chaque élément dans le jeu de données avant que le jeu de données ne soit trouvé.
-   Les tableaux de structures introduisent la nécessité d’une compréhension commune des informations transmises sur la partie de l’appelant et du composant. Ce besoin d’un mappage partagé entre deux éléments système peut entraîner des difficultés lors de la gestion de différentes versions de composants. Bien que la signature de la méthode ne change pas, les modifications apportées aux informations attendues peuvent rendre les programmes d’appel incompatibles.

Étant donné que les problèmes de complexité associés aux quatre méthodes de passage de paramètres sont tellement similaires, il est discutable qu’il existe une opportunité de simplification significative associée à une sélection.

## <a name="using-a-factory-pattern-to-pass-data"></a>Utilisation d’un modèle de fabrique pour passer des données

Un point de conception important est la simplicité d’utilisation. Le moment où vous avez décidé d’utiliser les jeux d’enregistrements ADO pour transmettre un ensemble structuré de détails à la couche présentation, vous avez introduit un problème de complexité. Les programmeurs de la couche présentation doivent comprendre la structure de ces jeux d’enregistrements. Un problème plus complexe peut survenir lorsque vous avez besoin de plusieurs détails pour un ensemble de données à transmettre dans un Recordset. Pour simplifier les choses, vous devez envisager de créer une méthode de fabrique d’objet Recordset chaque fois que vous envisagez de transmettre des données dans des jeux d’enregistrements ADO structurés.

La fabrique d’objets Recordset doit retourner un jeu d’enregistrements vide mais accessible en écriture à l’appelant. Ce jeu d’enregistrements doit avoir les champs appropriés (noms et types de données) déjà configurés afin que le client appelant n’ait pas besoin de savoir comment fabriquer le Recordset. Cette approche est souvent appelée *modèle de fabrique* et est un modèle de solution courant qui résout le besoin de créer un objet d’une complexité donnée sans avoir à connaître les nuances de sa création.

Les choix de conception simples, tels que le choix du même nom de paramètre pour le même élément de données, sur chaque méthode, où ces informations sont passées, facilitent l’examen d’une méthode et savent ce qui est attendu. Le fait de s’assurer que l’ordre dans lequel les arguments like sont passés est cohérent dans une famille de méthodes complète offre un point de confort qui applique un modèle cohérent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Optimisation des interactions entre le niveau de logique métier COM+ et la couche données](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




