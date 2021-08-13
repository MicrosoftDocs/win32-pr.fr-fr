---
description: Avec la technologie d’installation traditionnelle, il est nécessaire de quitter une application et de réexécuter le programme d’installation pour effectuer une tâche d’installation.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Installation à la demande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd20f83465fa110c4f749c6f11ba5ece1c6797a521174a8caebb9d152740aaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633868"
---
# <a name="installation-on-demand"></a>Installation à la demande

Avec la technologie d’installation traditionnelle, il est nécessaire de quitter une application et de réexécuter le programme d’installation pour effectuer une tâche d’installation. Cela se produit généralement lorsqu’un utilisateur souhaitait une fonctionnalité ou un produit qui n’a pas été choisi lors de la première exécution du programme d’installation. Cela rend souvent le processus de configuration du produit inefficace, car il a demandé à l’utilisateur d’anticiper les fonctionnalités requises avant qu’il n’ait jamais utilisé le produit.

L’installation à la demande permet d’offrir des fonctionnalités aux utilisateurs et aux applications en l’absence des fichiers eux-mêmes. Cette notion porte le nom de publication. le Windows Installer a la possibilité de publier des fonctionnalités et de rendre possible l’installation à la demande de fonctionnalités d’application ou de produits entiers. Lorsqu’un utilisateur ou une application active une fonctionnalité ou un produit publié, le programme d’installation se poursuit avec l’installation des composants nécessaires. Cela réduit le processus de configuration car des fonctionnalités supplémentaires sont accessibles sans avoir à quitter et à réexécuter une autre procédure d’installation.

Lorsqu’un produit utilise le programme d’installation, un utilisateur peut choisir, au moment de l’installation, les fonctionnalités ou les applications à installer et à publier. Puis, si lors de l’exécution d’une application, l’utilisateur demande une fonctionnalité publiée qui n’a pas encore été installée, l’application appelle le programme d’installation pour mettre en œuvre une installation de niveau de fonctionnalité juste-à-temps des fichiers nécessaires. Si l’utilisateur active un produit publié qui n’a pas encore été installé, le système d’exploitation appelle le programme d’installation pour mettre en œuvre une installation juste-à-temps du produit.

La [publication](advertisement.md) et l’installation-à la demande peuvent également faciliter la gestion du système en permettant aux administrateurs de désigner les applications comme requises ou facultatives pour différents groupes d’utilisateurs. Il existe deux types de publicité appelés « affectation » et « publication ». Si un administrateur attribue une application à un groupe, ces utilisateurs peuvent installer l’application à la demande. Toutefois, si l’administrateur publie l’application dans le groupe, aucun point d’entrée n’apparaît à ces utilisateurs et l’installation à la demande n’est activée que si une autre application active l’application publiée.

 

 



