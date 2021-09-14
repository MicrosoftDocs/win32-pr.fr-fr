---
description: L’état d’installation d’un fichier associé ne dépend pas de ses propres informations de contrôle de version de fichier, mais du contrôle de version de son parent associé.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Fichiers auxiliaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092137"
---
# <a name="companion-files"></a>Fichiers auxiliaires

L’état d’installation d’un fichier associé ne dépend pas de ses propres informations de contrôle de version de fichier, mais du contrôle de version de son parent associé. Consultez les [règles](file-versioning-rules.md)de contrôle de version des fichiers. Pour spécifier un fichier compagnon, la clé primaire du parent compagnon dans la [table file](file-table.md) doit être créée dans la colonne version de l’enregistrement pour le compagnon.

Dans l’exemple suivant, Filea est le parent associé et FileB est le fichier associé.

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Version |
|-------|---------|
| Filea | 1.0.0.0 |
| FileB | Filea   |



 

Dans cet exemple, l’état d’installation de FileB dépend des [règles](file-versioning-rules.md) de contrôle de version des fichiers et des informations de contrôle de version pour Filea. Si le programme d’installation détermine que la version de Filea dans le package doit être installée sur une version antérieure de Filea qui existe déjà sur l’ordinateur de l’utilisateur, il installera également FileB à partir du package, quelle que soit la version des FileB installés.

Notez qu’un fichier qui est le chemin d’accès de clé de son composant ne doit pas être un fichier auxiliaire. Cela entraînerait la logique de contrôle de version du fichier de chemin d’accès de clé qui est déterminée par le fichier parent associé.

 

 



