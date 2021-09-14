---
title: Nouvelle fonctionnalité historique des fichiers
description: Nouvelle fonctionnalité historique des fichiers
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293263"
---
# <a name="new-file-history-feature"></a>Nouvelle fonctionnalité historique des fichiers

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

La nouvelle fonctionnalité historique des fichiers remplace la fonction de sauvegarde et de restauration existante, et offre une protection pour les fichiers utilisateur stockés dans les bibliothèques utilisateur. Un ensemble d’API permettant aux développeurs d’activer l’historique des fichiers par programmation et de sélectionner une cible de stockage spécifique est fourni. La documentation relative à ces API est disponible sur MSDN.

cela peut affecter les flux de travail liés à la protection et à la documentation des données qui dépendent de la fonctionnalité de Sauvegarde Windows et de restauration.

Nous vous déconseillons d’utiliser les deux fonctionnalités en même temps. L’historique des fichiers vérifie s’il existe une planification de sauvegarde et qu’elle est active et si elle en trouve une, elle ne permet pas aux utilisateurs de l’activer. dans ce cas, les utilisateurs qui souhaitent utiliser l’historique des fichiers devront supprimer la planification de Sauvegarde Windows.

## <a name="manifestation"></a>Manifestation

les workflows peuvent être interrompus et la documentation de la méthode précédente pour accéder au Sauvegarde Windows et restaurer la fonctionnalité doit être mise à jour pour refléter ces modifications.

## <a name="solution"></a>Solution

Révisez les applications qui contiennent des flux de travail qui ont un impact négatif sur la nouvelle fonctionnalité historique des fichiers pour supprimer les conflits et incorporer le nouvel ensemble d’API.

## <a name="tests"></a>Tests

L’API permet aux développeurs de déterminer si l’historique des fichiers est activé.

 

 




