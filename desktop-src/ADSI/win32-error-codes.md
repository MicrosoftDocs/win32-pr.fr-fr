---
title: Codes d’erreur Win32
description: Le tableau suivant répertorie les messages d’erreur LDAP pour ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Codes d’erreur Win32 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d1986b0de2e4afeed0fccdcce62851acfaf104c3f360b7ea462410f4484f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118689889"
---
# <a name="win32-error-codes"></a>Codes d’erreur Win32

Le tableau suivant répertorie les messages d’erreur LDAP pour ADSI.



| Valeur d’erreur ADSI | Message LDAP                           | Message Win32                               | Description                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **\_succès LDAP**                      | **AUCUNE \_ erreur**                               | Opération réussie.                             |
| 0x80070005L      | **\_droits LDAP insuffisants \_**         | **ERREUR d' \_ accès \_ refusé**                   | L’utilisateur dispose de droits d’accès insuffisants.             |
| 0x80070008L      | **LDAP \_ pas de \_ mémoire**                   | **ERREUR \_ de \_ mémoire insuffisante \_**              | Mémoire système insuffisante.                         |
| 0x8007001fL      | **LDAP ( \_ autre)**                        | **\_échec de génération d’erreur \_**                     | Erreur inconnue.                                   |
| 0x800700eaL      | **\_résultats partiels LDAP \_**             | **ERREUR \_ plus de \_ données**                       | Résultats partiels et références reçues.          |
| 0x800700eaL      | **LDAP \_ \_ résultats supplémentaires \_ à \_ retourner**    | **ERREUR \_ plus de \_ données**                       | D’autres résultats doivent être retournés.                 |
| 0x800704c7L      | **annulation de l' \_ utilisateur LDAP \_**              | **ERREUR \_ annulée**                        | L’utilisateur a annulé l’opération.                     |
| 0x800704c9L      | **\_erreur de connexion LDAP \_**               | **ERREUR de \_ connexion \_ refusée**              | Impossible d’établir la connexion.                 |
| 0x8007052eL      | **\_ \_ informations d’identification LDAP non valides**         | **ERREUR \_ d’ouverture de session \_**                   | Les informations d’identification fournies ne sont pas valides.                |
| 0x800705b4L      | **\_délai d’expiration LDAP**                      | **\_délai d’erreur**                          | Délai de recherche dépassé.                                |
| 0x80071392L      | **LDAP \_ \_ existe déjà**              | **l' \_ objet d’erreur \_ \_ existe déjà**          | L’objet existe déjà.                           |
| 0x8007200aL      | **LDAP \_ non- \_ attribut de ce type \_**          | **ERREUR \_ DS \_ aucun \_ attribut \_ ou \_ valeur**     | L’attribut demandé n’existe pas.              |
| 0x8007200bL      | **\_syntaxe LDAP non valide \_**              | **ERREUR \_ de \_ \_ syntaxe d’attribut non valide du service d’annuaire \_**   | La syntaxe n’est pas valide.                             |
| 0x8007200cL      | **\_type LDAP non défini \_**              | **ERREUR \_ de \_ type d’attribut DS \_ \_ non défini**   | Type non défini.                                |
| 0x8007200dL      | **l' \_ attribut \_ ou la \_ valeur LDAP \_ existe** | **l' \_ attribut ou la valeur du service d’annuaire d’erreurs \_ \_ \_ \_ existe** | L’attribut existe ou la valeur a été assignée. |
| 0x8007200eL      | **LDAP \_ occupé**                         | **ERREUR \_ DS \_ occupé**                         | Le serveur est occupé.                                  |
| 0x8007200fL      | **LDAP \_ non disponible**                  | **ERREUR \_ DS \_ non disponible**                  | Le serveur n’est pas disponible.                         |
| 0x80072014L      | **\_violation de \_ classe d’objet LDAP \_**     | **ERREUR \_ de \_ \_ violation de classe obj du DS \_**        | Violation de classe d’objet.                          |
| 0x80072015L      | **LDAP \_ non \_ autorisé sur un non- \_ \_ Terminal**    | **ERREUR \_ DS \_ Impossible \_ sur un \_ non- \_ Terminal**          | L’opération n’est pas autorisée sur un objet non-feuille.  |
| 0x80072016L      | **LDAP \_ non \_ autorisé \_ sur \_ RDN**        | **ERREUR \_ DS \_ Impossible \_ sur \_ RDN**                | L’opération n’est pas autorisée sur un RDN.              |
| 0x80072017L      | **LDAP, \_ aucune \_ classe d’objet \_ \_ mods**      | **ERREUR DS inverser la \_ \_ \_ \_ \_ classe obj**        | Impossible de modifier la classe d’objet.                      |
| 0x80072020L      | **\_erreur des opérations LDAP \_**            | **erreur des opérations de l’annuaire d’erreurs \_ \_ \_**            | Une erreur d’opération s’est produite.                        |
| 0x80072021L      | **\_erreur de protocole LDAP \_**              | **erreur de \_ protocole du service d’annuaire \_ \_**              | Une erreur de protocole s’est produite.                         |
| 0x80072022L      | **\_TIMELIMIT LDAP \_ dépassé**          | **ERREUR \_ TIMELIMIT de l’annuaire de services \_ \_ dépassée**          | Limite de temps dépassée.                             |
| 0x80072023L      | **\_SIZELIMIT LDAP \_ dépassé**          | **ERREUR \_ SIZELIMIT de l’annuaire de services \_ \_ dépassée**          | Limite de taille dépassée.                             |
| 0x80072024L      | **\_limite d’administrateur LDAP \_ \_ dépassée**       | **ERREUR \_ de \_ limite d’administration DS \_ \_ dépassée**       | Limite d’administration dépassée sur le serveur.     |
| 0x80072025L      | **\_comparaison LDAP \_ false**               | **ERREUR de \_ comparaison des services d’annuaire \_ \_**               | Compare la **valeur false** obtenue.                       |
| 0x80072026L      | **\_comparaison LDAP \_ vrai**                | **ERREUR de \_ comparaison des services d’annuaire \_ \_**                | Compare la **valeur true**.                        |
| 0x80072027L      | **\_méthode d’authentification LDAP \_ \_ non \_ prise en charge** | **ERREUR \_ de \_ méthode d’authentification DS \_ \_ non \_ prise en charge** | La méthode d'authentification n'est pas prise en charge.      |
| 0x80072028L      | **\_authentification forte \_ LDAP \_ requise**       | **ERREUR d’authentification forte de l' \_ Annuaire de services \_ \_ \_ requise**       | Une authentification forte est requise.               |
| 0x80072029L      | **\_authentification non appropriée LDAP \_**          | **ERREUR \_ d' \_ authentification incorrecte DS \_**          | L’authentification n’est pas appropriée.                 |
| 0x8007202aL      | **\_authentification LDAP \_ inconnue**                | **ERREUR \_ d' \_ authentification DS \_ inconnue**                | Une erreur d’authentification inconnue s’est produite.           |
| 0x8007202bL      | **\_référence LDAP**                     | **Référence de l’annuaire d’erreurs \_ \_**                     | Impossible de résoudre la référence.                         |
| 0x8007202cL      | **\_extension de la \_ récriture LDAP non disponible \_** | **erreur d’extension d’erreur de \_ service d’annuaire \_ non disponible \_ \_** | L’extension critique n’est pas disponible.               |
| 0x8007202dL      | **\_confidentialité LDAP \_ requise**    | **confidentialité des erreurs du \_ service d’annuaire \_ \_ requise**    | La confidentialité est requise.                     |
| 0x8007202eL      | **\_correspondance non appropriée LDAP \_**      | **ERREUR \_ de \_ correspondance inappropriée DS \_**      | Une correspondance incorrecte a été créée.             |
| 0x8007202fL      | **\_violation de contrainte LDAP \_**        | **ERREUR \_ de \_ violation de contrainte DS \_**        | Une violation de contrainte s’est produite.                 |
| 0x80072030L      | **LDAP \_ non- \_ objet de ce type \_**             | **ERREUR \_ DS \_ non- \_ objet de ce type \_**             | L’objet n’existe pas.                           |
| 0x80072031L      | **\_problème d’alias LDAP \_**               | **ERREUR d' \_ alias du service d’annuaire \_ \_**               | L’alias n’est pas valide.                              |
| 0x80072032L      | **\_syntaxe DN non valide LDAP \_ \_**          | **ERREUR \_ DS \_ \_ syntaxe DN non valide \_**          | La syntaxe du nom unique n’est pas valide. |
| 0x80072033L      | **LDAP \_ est un \_ nœud terminal**                     | **l’erreur \_ DS \_ est \_ feuille**                     | L’objet est une feuille.                            |
| 0x80072034L      | **\_problème de \_ Deref d’alias LDAP \_**        | **ERREUR de l' \_ alias du service d’annuaire \_ \_ \_**        | Impossible de déréférencer l’alias.                    |
| 0x80072035L      | **le protocole LDAP \_ ne sera pas \_ \_ exécuté**       | **ERREUR \_ \_ \_ d’exécution du service d' \_ Annuaire**       | Le serveur ne peut pas effectuer l’opération.                 |
| 0x80072036L      | **\_détection de boucle LDAP \_**                 | **ERREUR \_ de \_ détection de boucle DS \_**                 | La boucle a été détectée.                               |
| 0x80072037L      | **\_violation de nommage LDAP \_**            | **ERREUR \_ de \_ violation d’appellation des services d’annuaire \_**            | Une violation de nom s’est produite.                    |
| 0x80072038L      | **\_résultats LDAP \_ trop \_ volumineux**          | **ERREUR de résultats de l' \_ \_ objet DS \_ \_ trop \_ grand**  | Le jeu de résultats est trop grand.                        |
| 0x80072039L      | **LDAP \_ affecte \_ plusieurs \_ DSA**      | **l’erreur \_ DS \_ affecte \_ plusieurs \_ DSA**      | Plusieurs agents de service d'annuaire sont affectés.  |
| 0x8007203aL      | **serveur LDAP en \_ \_ baisse**                 | **ERREUR \_ de \_ défaillance du serveur DS \_**                 | Impossible de contacter le serveur LDAP.                  |
| 0x8007203bL      | **\_erreur locale \_ LDAP**                 | **erreur de l’erreur \_ \_ locale DS \_**                 | Une erreur locale s’est produite.                            |
| 0x8007203cL      | **\_erreur d’encodage LDAP \_**              | **erreur \_ d' \_ encodage du service d’annuaire \_**              | Une erreur d’encodage s’est produite.                         |
| 0x8007203dL      | **\_erreur de décodage LDAP \_**              | **erreur \_ de \_ décodage du service d’annuaire \_**              | Une erreur de décodage s’est produite.                         |
| 0x8007203eL      | **\_Erreur du filtre LDAP \_**                | **ERREUR de \_ filtre de service d’annuaire \_ \_ inconnu**              | Le filtre de recherche est incorrect.                        |
| 0x8007203fL      | **\_erreur LDAP param \_**                 | **erreur \_ de \_ paramètre DS Error \_**                 | Un paramètre incorrect a été passé à une fonction.        |
| 0x80072040L      | **LDAP \_ non \_ pris en charge**               | **ERREUR \_ DS \_ non \_ prise en charge**               | Fonctionnalité non prise en charge.                           |
| 0x80072041L      | **LDAP \_ aucun \_ résultat \_ retourné**        | **ERREUR \_ DS \_ aucun \_ résultat \_ retourné**        | Les résultats ne sont pas retournés.                        |
| 0x80072042L      | **\_contrôle LDAP \_ \_ introuvable**          | **le contrôle de l’annuaire d’erreurs est \_ \_ \_ \_ introuvable**          | Le contrôle est introuvable.                           |
| 0x80072043L      | **\_boucle client \_ LDAP**                 | **ERREUR \_ de \_ boucle du client DS \_**                 | La boucle cliente a été détectée.                        |
| 0x80072044L      | **\_limite de redirection LDAP \_ \_ dépassée**    | **ERREUR \_ de \_ \_ dépassement de la limite de référence DS \_**    | Limite de redirection dépassée.                         |



 

 

 




