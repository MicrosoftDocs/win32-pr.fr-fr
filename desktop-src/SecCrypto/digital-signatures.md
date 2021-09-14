---
description: Les signatures numériques peuvent être utilisées pour distribuer un message sous forme de texte en clair lorsque les destinataires doivent identifier et vérifier l’expéditeur du message.
ms.assetid: 10c33787-72d3-4e5d-b4dd-633b3fd29903
title: Signatures numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d84d1a1c71b6b6d709dbe67b4fa2c81f4b54e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416488"
---
# <a name="digital-signatures"></a>Signatures numériques

Les [*signatures numériques*](../secgloss/d-gly.md) peuvent être utilisées pour distribuer un message sous forme de [*texte en clair*](../secgloss/p-gly.md) lorsque les destinataires doivent identifier et vérifier l’expéditeur du message. La signature d’un message ne modifie pas le message. il génère simplement une chaîne de signature numérique que vous pouvez regrouper avec le message ou transmettre séparément. Une signature numérique est un petit morceau de données qui est chiffré avec la [*clé privée*](../secgloss/p-gly.md)de l’expéditeur. Le déchiffrement des données de signature à l’aide de la [*clé publique*](../secgloss/p-gly.md) de l’expéditeur prouve que les données ont été chiffrées par l’expéditeur ou par une personne qui avait accès à la clé privée de l’expéditeur.

Les signatures numériques sont générées à l’aide d’algorithmes de signature de [*clé publique*](../secgloss/p-gly.md) . Une [*clé privée*](../secgloss/p-gly.md) génère la signature et la clé publique correspondante doit être utilisée pour valider la signature. Ce processus est illustré dans l’illustration suivante.

![génération d’une signature numérique](images/capi02.png)

La création d’une signature numérique à partir d’un message se fait en deux étapes. La première étape consiste à créer une valeur de [*hachage*](../secgloss/h-gly.md) (également appelée [*Résumé de message*](../secgloss/m-gly.md)) à partir du message. Cette valeur de hachage est ensuite signée à l’aide de la clé privée du signataire. L’illustration suivante présente les étapes nécessaires à la création d’une signature numérique.

![création d’une signature numérique à partir d’un message](images/capi06.png)

Pour vérifier une signature, le message et la signature sont requis. Tout d’abord, une valeur de hachage doit être créée à partir du message de la même façon que la signature a été créée. Cette valeur de hachage est ensuite vérifiée par rapport à la signature à l’aide de la clé publique du signataire. Si la valeur de hachage et la signature correspondent, vous pouvez être certain que le message est bien celui du signataire initialement signé et qu’il n’a pas été falsifié. Le diagramme suivant illustre le processus impliqué dans la vérification d’une signature numérique.

![vérification d’une signature numérique](images/capi07.png)

Une valeur de hachage se compose d’une petite quantité de données binaires, en général environ 160 bits. Cela se produit à l’aide d’un [*algorithme de hachage*](../secgloss/h-gly.md). Un certain nombre de ces algorithmes sont répertoriés plus loin dans cette section.

Toutes les valeurs de hachage partagent les propriétés suivantes, quel que soit l’algorithme utilisé :

-   La longueur de la valeur de hachage est déterminée par le type d’algorithme utilisé, et sa longueur ne varie pas en fonction de la taille du message. Les longueurs des valeurs de hachage les plus courantes sont 128 ou 160 bits.
-   Chaque paire de messages non identiques se traduit par une valeur de hachage complètement différente, même si les deux messages diffèrent uniquement par un seul bit. En utilisant la technologie d’aujourd’hui, il n’est pas possible de découvrir une paire de messages qui traduisent la même valeur de hachage sans rompre l’algorithme de hachage.
-   Chaque fois qu’un message particulier est haché à l’aide du même algorithme, la même valeur de hachage est générée.
-   Tous les algorithmes de hachage sont unidirectionnels. En raison d’une valeur de hachage, il n’est pas possible de récupérer le message d’origine. En fait, aucune des propriétés du message d’origine ne peut être déterminée étant donné la valeur de hachage seule.

 

 
