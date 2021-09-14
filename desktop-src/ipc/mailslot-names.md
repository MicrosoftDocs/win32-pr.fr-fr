---
description: Nommer des mailslots et placer des messages dans les mailslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Noms des mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292327"
---
# <a name="mailslot-names"></a>Noms des mailslot

Quand un processus crée un mailslot, le nom du mailslot doit se présenter sous la forme suivante.

\\\\.\\ nom du \\ \[ *chemin d’accès* mailslot \\ \] 

Un nom de mailslot requiert les éléments suivants : deux barres obliques inverses pour commencer le nom, un point, une barre oblique inverse après le point, le mot « mailslot » et une barre oblique inverse de fin. Les noms ne respectent pas la casse. Un nom de mailslot peut être précédé d’un chemin d’accès composé des noms d’un ou de plusieurs répertoires, séparés par des barres obliques inverses. Par exemple, si un utilisateur attend des messages sur les taxes de Bob, Pete et Sue, l’application mailslot de l’utilisateur peut autoriser l’utilisateur à créer des mailslots individuels pour chaque expéditeur, comme illustré ici :<dl> \\\\.\\ \\ \\ Commentaires bobs les taxes sur les mailslot \_  
\\\\.\\ \\commentaires des hypertaxations de mailslot \\ \_  
\\\\.\\ \\ \\ Commentaires écritures les taxes sur les mailslot \_  
</dl>

Pour placer un message dans un mailslot, un processus ouvre un mailslot par son nom. Pour écrire sur un serveur mailslot sur l’ordinateur local, un processus peut utiliser un nom de mailslot qui a la même forme que celle utilisée pour créer un mailslot. Toutefois, cette situation est relativement rare. Plus souvent, vous utiliserez le formulaire suivant pour écrire sur un serveur mailslot sur un ordinateur distant spécifique :

\\\\*Nom de l’ordinateur* \\ nom du \\ \[ *chemin d’accès* mailslot \\ \] 

Pour placer un message dans chaque mailslot dans le domaine spécifié avec un nom donné, utilisez la forme suivante :

\\\\*Nom_domaine* \\ nom du \\ \[ *chemin d’accès* mailslot \\ \] 

Pour placer un message dans chaque mailslot portant un nom donné dans le domaine principal du système, utilisez la forme suivante :

\\\\\*\\nom du \\ \[ *chemin d’accès* mailslot \\ \] 

 

 



