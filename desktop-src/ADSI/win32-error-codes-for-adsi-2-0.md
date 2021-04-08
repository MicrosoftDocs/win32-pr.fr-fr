---
title: Codes d’erreur Win32 pour ADSI 2,0
description: Le tableau suivant répertorie les messages d’erreur LDAP pour ADSI 2,0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Codes d’erreur Win32 pour ADSI 2,0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e079fa6a98df28625f6307f774ce194712a52a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839110"
---
# <a name="win32-error-codes-for-adsi-20"></a>Codes d’erreur Win32 pour ADSI 2,0

Le tableau suivant répertorie les messages d’erreur LDAP pour ADSI 2,0.



| Valeur d’erreur ADSI | Message LDAP                           | Message Win32                        | Description                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **\_succès LDAP**                      | **AUCUNE \_ erreur**                        | Opération réussie.                                 |
| 0x80070002       | **LDAP \_ non- \_ objet de ce type \_**             | **\_fichier d' \_ erreur \_ introuvable**          | L’objet n’existe pas.                               |
| 0x80070005       | **\_méthode d’authentification LDAP \_ \_ non \_ prise en charge** | **ERREUR d' \_ accès \_ refusé**            | Méthode d’authentification non prise en charge.                 |
| 0x80070005       | **\_authentification forte \_ LDAP \_ requise**       | **ERREUR d' \_ accès \_ refusé**            | Requiert une authentification forte.                      |
| 0x80070005       | **\_authentification non appropriée LDAP \_**          | **ERREUR d' \_ accès \_ refusé**            | Authentification inappropriée.                        |
| 0x80070005       | **\_droits LDAP insuffisants \_**         | **ERREUR d' \_ accès \_ refusé**            | L’utilisateur dispose de droits d’accès insuffisants.                 |
| 0x80070005       | **\_authentification LDAP \_ inconnue**                | **ERREUR d' \_ accès \_ refusé**            | Une erreur d’authentification inconnue s’est produite.               |
| 0x80070008       | **LDAP \_ pas de \_ mémoire**                   | **ERREUR \_ de \_ mémoire insuffisante \_**       | Mémoire système insuffisante.                             |
| 0x8007001F       | **LDAP ( \_ autre)**                        | **\_échec de génération d’erreur \_**              | Une erreur inconnue s’est produite.                              |
| 0x8007001F       | **\_erreur locale \_ LDAP**                 | **\_échec de génération d’erreur \_**              | Une erreur locale s’est produite.                                |
| 0x80070037       | **LDAP \_ non disponible**                  | **ERREUR \_ de \_ développement \_ inexistant**           | Le serveur n’est pas disponible.                             |
| 0x8007003A       | **serveur LDAP en \_ \_ baisse**                 | **ERREUR \_ de \_ réponse nette incorrecte \_**            | Impossible de contacter le serveur LDAP.                      |
| 0x8007003B       | **\_erreur d’encodage LDAP \_**              | **ERREUR \_ UNEXP \_ NET \_ Err**           | Une erreur d’encodage s’est produite.                             |
| 0x8007003B       | **\_erreur de décodage LDAP \_**              | **ERREUR \_ UNEXP \_ NET \_ Err**           | Une erreur de décodage s’est produite.                             |
| 0x80070044       | **\_limite d’administrateur LDAP \_ \_ dépassée**       | **ERREUR \_ de \_ noms trop nombreux \_**          | Limite d’administration dépassée sur le serveur.         |
| 0x80070056       | **\_ \_ informations d’identification LDAP non valides**         | **ERREUR \_ \_ de mot de passe non valide**         | Informations d’identification non valides.                                |
| 0x80070057       | **\_syntaxe DN non valide LDAP \_ \_**          | **paramètre d’erreur \_ non valide \_**        | La syntaxe du nom unique n’est pas valide.     |
| 0x80070057       | **\_violation de nommage LDAP \_**            | **paramètre d’erreur \_ non valide \_**        | Violation d’attribution de noms.                                    |
| 0x80070057       | **\_violation de \_ classe d’objet LDAP \_**     | **paramètre d’erreur \_ non valide \_**        | Violation de classe d’objet.                              |
| 0x80070057       | **\_Erreur du filtre LDAP \_**                | **paramètre d’erreur \_ non valide \_**        | Le filtre de recherche est incorrect.                                |
| 0x80070057       | **\_erreur LDAP param \_**                 | **paramètre d’erreur \_ non valide \_**        | Un paramètre incorrect a été passé à une routine.               |
| 0X8007006E       | **\_erreur des opérations LDAP \_**            | **échec de l’ouverture de l’erreur \_ \_**              | Une erreur d’opération s’est produite.                            |
| 0x8007007A       | **\_résultats LDAP \_ trop \_ volumineux**          | **ERREUR \_ de \_ mémoire tampon insuffisante**      | Le jeu de résultats est trop grand.                            |
| 0x8007007B       | **\_syntaxe LDAP non valide \_**              | **ERREUR \_ nom non valide \_**             | Syntaxe non valide.                                    |
| 0x8007007C       | **\_erreur de protocole LDAP \_**              | **niveau d’erreur \_ non valide \_**            | Erreur de protocole.                                      |
| 0x800700B7       | **LDAP \_ \_ existe déjà**              | **l' \_ erreur \_ existe déjà**           | L’objet existe déjà.                               |
| 0x800700EA       | **\_résultats partiels LDAP \_**             | **ERREUR \_ plus de \_ données**                | Résultats partiels et références reçues.              |
| 0x800700EA       | **LDAP \_ occupé**                         | **ERREUR de \_ disponibilité**                      | Le serveur est occupé.                                      |
| 0x800703EB       | **le protocole LDAP \_ ne sera pas \_ \_ exécuté**       | **l' \_ erreur \_ ne peut pas se \_ terminer**        | Le serveur ne peut pas effectuer l’opération.                     |
| 0x8007041D       | **\_délai d’expiration LDAP**                      | **ERREUR \_ de \_ \_ délai d’expiration de la demande de service** | Délai de recherche dépassé.                                    |
| 0x800704B8       | **\_comparaison LDAP \_ false**               | **erreur \_ étendue d’erreur \_**           | Compare la **valeur false** obtenue.                           |
| 0x800704B8       | **\_comparaison LDAP \_ vrai**                | **erreur \_ étendue d’erreur \_**           | Compare la **valeur true**.                            |
| 0x800704B8       | **\_référence LDAP**                     | **erreur \_ étendue d’erreur \_**           | Impossible de résoudre la référence.                             |
| 0x800704B8       | **\_extension de la \_ récriture LDAP non disponible \_** | **erreur \_ étendue d’erreur \_**           | L’extension critique n’est pas disponible.                   |
| 0x800704B8       | **LDAP \_ non- \_ attribut de ce type \_**          | **erreur \_ étendue d’erreur \_**           | L’attribut demandé n’existe pas.                  |
| 0x800704B8       | **\_type LDAP non défini \_**              | **erreur \_ étendue d’erreur \_**           | Le type n’est pas défini.                                 |
| 0x800704B8       | **\_correspondance non appropriée LDAP \_**      | **erreur \_ étendue d’erreur \_**           | Une correspondance incorrecte a été créée.                 |
| 0x800704B8       | **\_violation de contrainte LDAP \_**        | **erreur \_ étendue d’erreur \_**           | Une violation de contrainte s’est produite.                     |
| 0x800704B8       | **l' \_ attribut \_ ou la \_ valeur LDAP \_ existe** | **erreur \_ étendue d’erreur \_**           | L'attribut existe ou la valeur a été assignée. |
| 0x800704B8       | **\_problème d’alias LDAP \_**               | **erreur \_ étendue d’erreur \_**           | L’alias n’est pas valide.                                  |
| 0x800704B8       | **LDAP \_ est un \_ nœud terminal**                     | **erreur \_ étendue d’erreur \_**           | L’objet est une feuille.                                    |
| 0x800704B8       | **\_problème de \_ Deref d’alias LDAP \_**        | **erreur \_ étendue d’erreur \_**           | Impossible de déréférencer l’alias.                        |
| 0x800704B8       | **\_détection de boucle LDAP \_**                 | **erreur \_ étendue d’erreur \_**           | La boucle a été détectée.                                   |
| 0x800704B8       | **LDAP \_ non \_ autorisé sur un non- \_ \_ Terminal**    | **erreur \_ étendue d’erreur \_**           | L’opération n’est pas autorisée sur un objet non-feuille.       |
| 0x800704B8       | **LDAP \_ non \_ autorisé \_ sur \_ RDN**        | **erreur \_ étendue d’erreur \_**           | L’opération n’est pas autorisée sur le RDN.                     |
| 0x800704B8       | **LDAP, \_ aucune \_ classe d’objet \_ \_ mods**      | **erreur \_ étendue d’erreur \_**           | Impossible de modifier la classe d’objet.                          |
| 0x800704B8       | **LDAP \_ affecte \_ plusieurs \_ DSA**      | **erreur \_ étendue d’erreur \_**           | Plusieurs agents de service d'annuaire sont affectés.      |
| 0x800704C7       | **annulation de l' \_ utilisateur LDAP \_**              | **ERREUR \_ annulée**                 | L’utilisateur a annulé l’opération.                     |
| 0x80070718       | **\_TIMELIMIT LDAP \_ dépassé**          | **QUOTA d’erreur \_ \_ insuffisante \_**        | Limite de temps dépassée.                                 |
| 0x80070718       | **\_SIZELIMIT LDAP \_ dépassé**          | **QUOTA d’erreur \_ \_ insuffisante \_**        | Limite de taille dépassée.                                 |



 

Dans ADSI 2,0, plusieurs messages d’erreur LDAP sont mappés à un code d’erreur Win32 en tant qu’erreur **étendue d’erreur \_ \_**. Appelez [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) pour récupérer la chaîne d’erreur retournée par le serveur. Pour plus d’informations, consultez [les messages d’erreur étendus ADSI](adsi-extended-error-messages.md) ci-dessous.

 

 




