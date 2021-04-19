---
description: Contrôle parental et contrôle de compte d’utilisateur
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Contrôle parental et contrôle de compte d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541208"
---
# <a name="parental-controls-and-user-account-control"></a>Contrôle parental et contrôle de compte d’utilisateur

Le contrôle de compte d’utilisateur (UAC) entraîne la présence de comptes d’utilisateur standard et d’administrateur protégé. Un administrateur protégé s’exécute avec les mêmes droits qu’un utilisateur standard dans le cadre d’une utilisation normale. Pour les opérations privilégiées :

-   Un utilisateur standard affiche la boîte de dialogue informations d’identification de l’interface utilisateur, qui requiert l’entrée d’un nom d’utilisateur et d’un mot de passe pour un administrateur protégé ou un administrateur intégré.
-   Un administrateur protégé s’affichera dans la boîte de dialogue de l’interface utilisateur de consentement, ce qui nécessite de sélectionner autoriser pour continuer.

Il est important de noter que le contrôle de compte d’utilisateur est implémenté par processus, ce qui signifie qu’un processus s’exécute avec élévation de privilèges ou non. En règle générale, il ne convient pas du point de vue de la sécurité pour exécuter des applications volumineuses comme toujours élevés. Pour les contrôles de contrôle parental, le code qui doit modifier les paramètres doit être isolé par l’une des deux options d’implémentation :

1.  Créez un petit exécutable pour la gestion des paramètres qui est marqué dans son manifeste comme nécessitant des droits d’administration. L’appel de l’exécutable entraîne l’affichage de l’interface utilisateur de consentement ou d’informations d’identification avant d’autoriser l’exécution du processus.
2.  Fournissez des interfaces COM dans une DLL de produit qui autorisent l’appel par documentation UAC. Cela entraînera également l’affichage de l’interface utilisateur de consentement ou d’informations d’identification appropriée.

 

 



