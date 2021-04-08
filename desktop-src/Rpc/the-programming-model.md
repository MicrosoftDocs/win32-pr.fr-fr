---
title: Le modèle de programmation
description: Au début de la programmation informatique, chaque programme était écrit sous la forme d’un grand segment monolithique, rempli d’instructions goto.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673462"
---
# <a name="the-programming-model"></a>Le modèle de programmation

Au début de la programmation informatique, chaque programme était écrit sous la forme d’un grand segment monolithique, rempli d’instructions **goto** . Chaque programme devait gérer ses propres entrées et sorties sur différents périphériques matériels. À mesure que la discipline de programmation a évolué, ce code monolithique a été organisé en procédures, avec les procédures les plus couramment utilisées dans les bibliothèques pour le partage et la réutilisation.

![instructions goto monolithiques et procédures empaquetées dans des bibliothèques partagées](images/prog-a06.png)

Le langage de programmation C prend en charge la programmation orientée procédure. En C, la procédure principale est associée à toutes les autres procédures en tant que cases noires. Par exemple, la procédure main ne peut pas déterminer comment les procédures A, B et X effectuent leur travail. La procédure main n’appelle qu’une autre procédure. elle ne contient pas d’informations sur l’implémentation de cette procédure.

![isolement des activités effectuées dans les procédures externes](images/prog-a08.png)

Les langages de programmation orientés procédure fournissent des mécanismes simples pour spécifier et écrire des procédures. Par exemple, le prototype de fonction C ANSI-standard est une construction utilisée pour spécifier le nom d’une procédure, le type du résultat qu’elle retourne (le cas échéant) et le nombre, la séquence et le type de ses paramètres. L’utilisation du prototype de fonction est un moyen formel de spécifier une interface entre des procédures.

Microsoft RPC s’appuie sur ce modèle de programmation en permettant aux procédures, regroupées dans les interfaces, de résider dans des processus différents de l’appelant. Microsoft RPC ajoute également une approche plus formelle de la définition de la procédure qui permet à l’appelant et à la routine appelée d’adopter un contrat pour échanger des données à distance et appeler des fonctionnalités. Dans le modèle de programmation Microsoft RPC, les appels de fonction traditionnels sont complétés par deux éléments supplémentaires.

-   Le premier élément est un fichier. idl/. ACF qui décrit précisément le mécanisme d’échange de données et de passage de paramètres entre l’appelant et la procédure appelée.
-   Le deuxième élément est un ensemble d’API d’exécution qui fournissent aux développeurs un contrôle granulaire de l’appel de procédure distante, y compris des aspects de sécurité, la gestion de l’État sur le serveur, la spécification des clients qui peuvent communiquer avec le serveur, et ainsi de suite.

 

 




