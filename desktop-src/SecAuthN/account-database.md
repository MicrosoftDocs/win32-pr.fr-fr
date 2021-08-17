---
description: Active Directory fournit la base de données de comptes que le centre de distribution de clés (KDC) utilise pour obtenir des informations sur les principaux de sécurité dans le domaine.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Base de données du compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4d5e41c959a8c546ef36a5e4014b14ffc949e1670e2b32b199a8c9368bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141592"
---
# <a name="account-database"></a>Base de données du compte

Active Directory fournit la base de données de comptes que le [*Centre de distribution de clés*](/windows/desktop/SecGloss/k-gly) (KDC) utilise pour obtenir des informations sur les [*principaux de sécurité*](/windows/desktop/SecGloss/s-gly) dans le domaine. Chaque principal est représenté par un objet de compte dans le répertoire. La clé de [*chiffrement*](/windows/desktop/SecGloss/e-gly) utilisée pour communiquer avec un utilisateur, un ordinateur ou un service est stockée en tant qu’attribut de l’objet de compte de ce principal de sécurité.

Seuls les contrôleurs de domaine sont des serveurs Active Directory. Chaque contrôleur de domaine conserve une copie accessible en écriture de l’annuaire, ce qui permet de créer des comptes, de réinitialiser les mots de passe et de modifier l’appartenance aux groupes dans n’importe quel contrôleur de domaine. Les modifications apportées à un réplica de l’annuaire sont propagées automatiquement à tous les autres réplicas. Windows réplique la banque d’informations du Active Directory à l’aide d’un protocole propriétaire de réplication à plusieurs maîtres qui utilise une connexion d’appel de procédure distante sécurisée entre des partenaires de réplication. La connexion utilise le [*protocole d’authentification Kerberos*](/windows/desktop/SecGloss/k-gly) pour fournir une [*authentification*](/windows/desktop/SecGloss/a-gly) mutuelle et un chiffrement.

Le stockage physique des données de compte est géré par l' [agent de système d’annuaire](/windows/desktop/AD/directory-system-agent), un processus protégé intégré à l’autorité de [*sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) sur le contrôleur de domaine. Les clients du service d’annuaire ne disposent jamais d’un accès direct au magasin de données. Tout client qui souhaite accéder aux informations d’annuaire doit se connecter à l’agent de système d’annuaire, puis rechercher, lire et écrire des objets d’annuaire et leurs attributs.

les demandes d’accès à un objet ou un attribut dans l’annuaire sont soumises à validation par Windows mécanismes de contrôle d’accès. À l’instar des objets fichier et dossier du système de fichiers NTFS, les objets du Active Directory sont protégés par des [*listes de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) qui spécifient qui peut accéder à l’objet et de quelle manière. Contrairement aux fichiers et dossiers, toutefois, les objets Active Directory ont une liste de contrôle d’accès pour chacun de leurs attributs. Ainsi, les attributs des informations de compte sensibles peuvent être protégés par des autorisations plus restrictives que celles accordées aux autres attributs du compte.

Les informations les plus sensibles sur un compte sont naturellement son mot de passe. Bien que l’attribut de mot de passe d’un objet de compte stocke une clé de chiffrement dérivée d’un mot de passe, et non le mot de passe lui-même, cette clé est tout aussi utile pour un intrus. Par conséquent, l’accès à l’attribut de mot de passe d’un objet de compte est accordé uniquement au détenteur du compte, jamais à toute personne, et pas même aux administrateurs. Seuls les processus avec un privilège Trusted Computing base (processus en cours d’exécution dans le [*contexte*](/windows/desktop/SecGloss/c-gly) de sécurité de l’autorité de certification locale) sont autorisés à lire ou à modifier les informations de mot de passe.

Pour empêcher une attaque hors connexion d’un utilisateur ayant accès à la bande de sauvegarde d’un contrôleur de domaine, l’attribut de mot de passe d’un objet de compte est protégé par un deuxième chiffrement à l’aide d’une clé système. Cette clé de chiffrement peut être stockée sur un support amovible afin de pouvoir être sauvegardée séparément, ou elle peut être stockée sur le contrôleur de domaine, mais protégée par un mécanisme de dispersion. Les administrateurs ont la possibilité de choisir l’emplacement de stockage de la clé système et les algorithmes utilisés pour chiffrer les attributs de mot de passe.

 

 
