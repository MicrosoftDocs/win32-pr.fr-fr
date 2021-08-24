---
description: Les packages d’authentification sont contenus dans les bibliothèques de liens dynamiques.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Packages d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d556489d520ebf45224e3e9b8a5526cc4debcf1c7e7ab95028ecd9e35a6de217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141362"
---
# <a name="authentication-packages"></a>Packages d’authentification

Les [*packages d’authentification*](/windows/desktop/SecGloss/a-gly) sont contenus dans les bibliothèques de liens dynamiques. L' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) charge les packages d’authentification à l’aide des informations de configuration stockées dans le registre. Le chargement de plusieurs packages d’authentification permet à l’autorité LSA de prendre en charge plusieurs processus d’ouverture de session et plusieurs [*protocoles de sécurité*](/windows/desktop/SecGloss/s-gly).

Les processus d’ouverture de session utilisent des packages d’authentification pour analyser les données de connexion. De nouveaux processus d’ouverture de session sont ajoutés à un système en ajoutant un [*Gina*](/windows/desktop/SecGloss/g-gly) pour collecter les données de connexion requises et, si nécessaire, en ajoutant un nouveau package d’authentification pour analyser les données.

Les protocoles de sécurité sont implémentés par des packages d’authentification. Un package d’authentification analyse les données de connexion en suivant les règles et procédures stipulées dans un protocole de sécurité.

Les packages d’authentification sont responsables des tâches suivantes :

-   Analyse des données de connexion pour déterminer si un [*principal de sécurité*](/windows/desktop/SecGloss/s-gly) est autorisé à se connecter à un système.
-   Établissement d’une nouvelle [*session de connexion*](/windows/desktop/SecGloss/l-gly) et création d’un identificateur de [*connexion*](/windows/desktop/SecGloss/l-gly) unique pour le principal authentifié avec succès.
-   Passage des informations de sécurité à LSA pour le jeton de sécurité du principal.

Lorsqu’un utilisateur tente une ouverture de session interactive, le LSA appelle un package d’authentification pour déterminer s’il faut autoriser l’utilisateur à se connecter. \_par exemple, MSV1 0 est un package d’authentification installé avec le système d’exploitation Microsoft Windows. Le \_ package MSV1 0 accepte un nom d’utilisateur et un mot de passe [*haché*](/windows/desktop/SecGloss/h-gly) . Il recherche la combinaison nom d’utilisateur et mot de passe haché dans la base de données du gestionnaire de comptes de sécurité (SAM). Si les données de connexion correspondent aux [*informations d’identification*](/windows/desktop/SecGloss/c-gly)stockées, le package d’authentification permet à l’ouverture de session de se dérouler correctement.

Une fois les informations d’identification d’un [*principal de sécurité*](/windows/desktop/SecGloss/s-gly) authentifiées, un package d’authentification est responsable de la création d’une nouvelle session LSA pour le principal et de l’allocation de l' [*identificateur de connexion*](/windows/desktop/SecGloss/l-gly) qui identifie de façon unique la session de connexion. Le package d’authentification peut associer les informations d’identification à la session de connexion pour les demandes d’authentification ultérieures. Par exemple, le \_ package d’authentification MSV1 0 (fourni par Microsoft) associe le nom du compte d’utilisateur et un hachage du mot de passe de l’utilisateur à chaque ouverture de session.

Le package d’authentification fournit également un ensemble d' [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) et d’autres informations appropriées pour l’inclusion dans le jeton de sécurité créé par l’autorité LSA. ce jeton représente le [*contexte*](/windows/desktop/SecGloss/c-gly) de sécurité du principal pour l’accès aux opérations de Windows.

Une fois qu’une session de connexion est créée et associée à un principal, les demandes d’authentification ultérieures effectuées pour le compte du principal sont gérées différemment de la connexion initiale. Le package d’authentification ne crée pas de nouvelle session d’ouverture de session et ne retourne pas d’informations pour la création d’un jeton. Le package d’authentification peut, toutefois, associer des [*informations d’identification supplémentaires*](/windows/desktop/SecGloss/s-gly) obtenues lors d’une authentification ultérieure avec la session d’ouverture de session existante du principal. Les informations d’identification supplémentaires sont obtenues lorsque l’accès à une ressource demandée nécessite des informations au-delà des informations d’identification établies par l’ouverture de session initiale. Par exemple, lorsqu’un utilisateur connecté demande une ouverture de session réseau Novell, un package d’authentification spécifique à Novell peut être appelé et les informations d’identification spécifiques à Novell peuvent être authentifiées et associées à la session d’ouverture de session. Ces informations d’identification peuvent être référencées par un redirecteur Novell (par le biais du package d’authentification Novell) lorsque l’utilisateur accède au réseau Novell.

Les rubriques suivantes abordent les différents types de [*packages d’authentification*](/windows/desktop/SecGloss/a-gly):

-   [Windows Packages d’authentification](windows-authentication-packages.md)
-   [Fournisseur de support de sécurité/packages d’authentification](security-support-provider-authentication-packages.md)
-   [Packages d’authentification fournis par Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Packages de sous-authentification](subauthentication-packages.md)

 

 
