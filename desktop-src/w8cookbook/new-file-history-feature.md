---
title: Nouvelle fonctionnalité historique des fichiers
description: Nouvelle fonctionnalité historique des fichiers
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1502450c1376a57f9de99badc5188c8ce07761e0c28ae3ac2245a84437b5e66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932189"
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

 

 




