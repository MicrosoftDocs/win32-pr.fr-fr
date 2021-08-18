---
description: Filtres de mot de passe
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtres de mot de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5771fce0e8cbb2826bcf79344e2813587db6dcedc831d7e879b42ab74698b9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893999"
---
# <a name="password-filters"></a>Filtres de mot de passe

Les filtres de mot de passe vous permettent d’implémenter une stratégie de mot de passe et une notification de modification.

Quand une demande de modification de mot de passe est effectuée, l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) appelle les filtres de mot de passe inscrits sur le système. Chaque filtre de mot de passe est appelé deux fois : tout d’abord pour valider le nouveau mot de passe, puis, une fois que tous les filtres ont validé le nouveau mot de passe, pour informer les filtres que la modification a été apportée. L'illustration ci-dessous montre ce processus.

![demande de modification de mot de passe](images/pswdfilte.png)

La notification de modification de mot de passe est utilisée pour synchroniser les modifications de mot de passe dans les bases de données de comptes.

Les filtres de mot de passe sont utilisés pour appliquer la stratégie de mot de passe. Les filtres valident les nouveaux mots de passe et indiquent si le nouveau mot de passe est conforme à la stratégie de mot de passe implémentée.

Pour une vue d’ensemble de l’utilisation des filtres de mot de passe, consultez [utilisation de filtres de mot de passe](using-password-filters.md).

Pour obtenir la liste des fonctions de filtre de mot de passe, consultez [fonctions de filtre de mot de passe](management-functions.md).

Les rubriques suivantes fournissent des informations supplémentaires sur les filtres de mot de passe :

-   [Considérations sur la programmation du filtre de mot de passe](password-filter-programming-considerations.md)
-   [Mise en œuvre des mots de passe forts et Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
