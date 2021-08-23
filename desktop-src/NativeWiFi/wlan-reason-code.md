---
description: Indique la raison de l’échec d’une opération de réseau local sans fil.
ms.assetid: 7b267f0b-b3f7-4729-bab4-de3bdd0a35a2
title: WLAN_REASON_CODE (wlanapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f24b0ab902610408eb7b80b4a962fcc81d4598244714b8f30f0ebf350a7e628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064559"
---
# <a name="wlan_reason_code"></a>\_Code de raison WLAN \_

Le type de **\_ \_ Code motif WLAN** indique la raison de l’échec d’une opération de réseau local sans fil.

Vous pouvez utiliser la fonction [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring) pour mapper un code de raison numérique (par exemple, 0x00050007) à sa signification textuelle. Vous pouvez également utiliser la table de recherche pour faciliter l’interprétation de la valeur numérique du code de raison. pour afficher la table de recherche, consultez l’annexe E : mappage des codes de raison aux messages d’événement dans le document [résolution des problèmes Windows les connexions sans fil Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10)).


```C++
typedef DWORD WLAN_REASON_CODE, *PWLAN_REASON_CODE;
```



Le tableau suivant répertorie les codes d’erreur généraux.



| Code de la raison                 | Signification                            |
|-----------------------------|------------------------------------|
| \_succès du \_ Code de raison WLAN \_ | L’opération a échoué.            |
| \_Code du motif WLAN \_ \_ inconnu | La raison de l’échec est inconnue. |



 

Le tableau suivant répertorie les codes d’erreur de configuration automatique.



| Code de raison                                  | Signification                                         |
|----------------------------------------------|-------------------------------------------------|
| \_réseau du \_ Code motif WLAN \_ \_ non \_ compatible | Le réseau sans fil n’est pas compatible.         |
| \_Profil du motif WLAN \_ \_ \_ non \_ compatible | Le profil de réseau sans fil n’est pas compatible. |



 

Le tableau suivant répertorie les codes d’erreur de connexion automatique.



| Code de raison                                                | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Code motif \_ WLAN \_ sans \_ \_ connexion automatique                   | Le profil ne spécifie aucune connexion automatique.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_Code de raison WLAN \_ \_ non \_ visible                           | Le réseau sans fil n’est pas visible.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Code de raison du WLAN \_ \_ \_ \_ refusé                             | Le réseau sans fil est bloqué par la stratégie de groupe.                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_Code motif WLAN refusé par l' \_ \_ utilisateur \_                           | Le réseau sans fil est bloqué par l’utilisateur.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_type de motif de raison WLAN \_ \_ \_ \_ non \_ autorisé                | Le type BSS (Basic Service Set) n’est pas autorisé sur cette carte sans fil.                                                                                                                                                                                                                                                                                                                                                                               |
| \_ \_ Code de raison WLAN dans la \_ \_ liste des échecs \_                       | Le réseau sans fil est dans la liste des échecs.                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ Code de raison WLAN dans la \_ \_ liste bloquée \_                      | Le réseau sans fil est dans la liste des connexions bloquées.                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_Code motif \_ WLAN \_ liste des SSID \_ \_ trop \_ longs                  | La taille de la liste des identificateurs de jeu de services (SSID) dépasse la taille maximale prise en charge par l’adaptateur.                                                                                                                                                                                                                                                                                                                                                  |
| échec de l' \_ appel de connexion du code de raison WLAN \_ \_ \_ \_                    | L’appel de connexion MSM (Media specific module) échoue.                                                                                                                                                                                                                                                                                                                                                                                                     |
| échec de l’appel de l’analyse du code de \_ raison WLAN \_ \_ \_ \_                       | L’appel de l’analyse MSM échoue.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_réseau du \_ Code motif WLAN \_ \_ non \_ disponible                | Le réseau spécifié n’est pas disponible. Ce code de raison est également utilisé en cas d’incompatibilité entre les fonctionnalités spécifiées dans un profil XML et les fonctionnalités d’interface et/ou de réseau. Par exemple, si un profil spécifie l’utilisation de WPA2 lorsque la carte réseau ne prend en charge que WPA, ce code d’erreur est renvoyé. En outre, si un profil spécifie l’utilisation du mode FIPS lorsque la carte réseau ne prend pas en charge le mode FIPS, ce code d’erreur est renvoyé.<br/> |
| \_raison WLAN \_ \_ profil de code de motif \_ modifié \_ ou \_ supprimé          | Le profil a été modifié ou supprimé avant l’établissement de la connexion.                                                                                                                                                                                                                                                                                                                                                                               |
| incompatibilité de clé de code de \_ raison WLAN \_ \_ \_                          | La clé de profil ne correspond pas à la clé réseau.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_Code motif WLAN l' \_ \_ utilisateur \_ ne \_ répond pas                     | L’utilisateur ne répond pas.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_motif WLAN \_ code \_ AP \_ \_ non \_ autorisé pour le \_ \_ client | Une application a tenté d’appliquer un profil de réseau hébergé sans fil à une carte réseau sans fil physique à l’aide de la fonction [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , plutôt qu’à un appareil virtuel.                                                                                                                                                                                                                                                    |
| \_motif WLAN \_ code \_ AP \_ \_ non \_ autorisé              | Une application a tenté d’appliquer un profil de réseau hébergé sans fil à une carte réseau sans fil physique à l’aide de la fonction [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) , plutôt qu’à un appareil virtuel.                                                                                                                                                                                                                                                    |



 

Le tableau suivant répertorie les codes d’erreur de validation de profil.



| Code de raison                                                    | Signification                                                                                                                                                                                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Code motif WLAN- \_ \_ schéma de profil non valide \_ \_                   | Le profil n’est pas valide selon le schéma.                                                                                                                                                                                                  |
| \_Profil du motif WLAN \_ \_ \_ manquant                           | L’élément WLANProfile est manquant.                                                                                                                                                                                                           |
| \_Code motif \_ WLAN \_ \_ nom du profil non valide \_                     | Le nom du profil n’est pas valide.                                                                                                                                                                                                           |
| \_Code motif WLAN- \_ \_ type de profil non valide \_ \_                     | Le type du profil n’est pas valide.                                                                                                                                                                                                           |
| \_Code motif WLAN- \_ \_ \_ type PHY non valide \_                         | Le type PHY n’est pas valide.                                                                                                                                                                                                                      |
| \_Code motif \_ WLAN \_ \_ sécurité MSM \_ manquant                     | Les paramètres de sécurité MSM sont manquants.                                                                                                                                                                                                        |
| \_Code motif \_ WLAN \_ \_ sécurité IHV \_ non \_ prise en charge              | Les paramètres de sécurité du fournisseur de matériel indépendant (IHV) sont manquants.                                                                                                                                                                          |
| \_raison WLAN \_ code \_ d' \_ incompatibilité de fabricant de matériel \_                         | Le profil de IHV OUI ne correspond pas à l’adaptateur OUI.                                                                                                                                                                                       |
| \_raison WLAN \_ Code de fabricant de \_ matériel \_ Oui \_ manquant                          | Les paramètres de l’OUI IHV sont manquants.                                                                                                                                                                                                             |
| \_raison WLAN \_ - \_ \_ paramètres IHV \_ manquants                     | Les paramètres de sécurité IHV sont manquants.                                                                                                                                                                                                        |
| \_Code motif \_ WLAN \_ \_ connectivité IHV \_ non \_ prise en charge          | Une application a tenté d’appliquer un profil IHV sur un adaptateur qui ne prend pas en charge les paramètres de connectivité IHV.                                                                                                                                   |
| \_sécurité des \_ conflits de code de motif WLAN \_ \_                         | Les paramètres de sécurité sont en conflit.                                                                                                                                                                                                               |
| \_sécurité du \_ Code motif WLAN \_ \_ manquante                          | Les paramètres de sécurité sont manquants.                                                                                                                                                                                                            |
| \_Code motif \_ WLAN \_ \_ type BSS non valide \_                         | Le type BSS n’est pas valide.                                                                                                                                                                                                                    |
| \_Code motif \_ WLAN \_ \_ mode de \_ connexion adhoc non valide \_           | Impossible de définir la connexion automatique pour un réseau ad hoc.                                                                                                                                                                                     |
| \_Code motif \_ WLAN \_ non \_ diffusion \_ défini \_ pour \_ ad hoc            | Impossible de définir une non-diffusion pour un réseau ad hoc.                                                                                                                                                                                            |
| \_ \_ \_ commutateur automatique du code motif WLAN \_ \_ défini \_ pour \_ ad hoc              | Le commutateur automatique ne peut pas être défini pour un réseau ad hoc.                                                                                                                                                                                              |
| \_ \_ \_ commutateur automatique du code motif WLAN \_ \_ défini \_ pour la \_ \_ connexion manuelle | Impossible de définir le commutateur automatique pour un profil de connexion manuel.                                                                                                                                                                                    |
| \_Code motif \_ WLAN \_ sécurité IHV- \_ sécurité \_ Onex \_ manquante               | Les paramètres de sécurité IHV 802.1 X sont manquants.                                                                                                                                                                                                 |
| \_SSID du profil de motif WLAN \_ \_ \_ \_ non valide                     | Le SSID dans le profil n’est pas valide ou est manquant.                                                                                                                                                                                                |
| \_Code de raison WLAN trop d' \_ \_ \_ \_ identificateur SSID                            | Un trop grand nombre d’identificateurs SSID ont été spécifiés dans le profil.                                                                                                                                                                                                 |
| \_Code motif \_ WLAN \_ \_ connectivité IHV \_ non \_ prise en charge          |                                                                                                                                                                                                                                               |
| \_Code motif \_ WLAN \_ \_ nombre maximal \_ de clients erronés pour le \_ \_ point de \_ vue \_     | Une application a essayé d’appliquer un profil de réseau hébergé sans fil à une carte réseau physique à l’aide de la fonction [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) et a spécifié une valeur inacceptable pour le nombre maximal de clients autorisés. |
| \_Code de motif WLAN \_ \_ canal non valide \_                           | Le canal spécifié n’est pas valide.                                                                                                                                                                                                             |
| \_mode de fonctionnement du code de raison WLAN \_ \_ \_ \_ non \_ pris en charge            |                                                                                                                                                                                                                                               |
| le \_ profil de raison du WLAN \_ code \_ auto \_ AP \_ \_ non \_ autorisé            | Une erreur interne du système d’exploitation s’est produite avec le réseau hébergé sans fil.                                                                                                                                                                 |
| \_connexion automatique du code de raison WLAN \_ \_ \_ \_ non \_ autorisée             |                                                                                                                                                                                                                                               |



 

Le tableau suivant répertorie les codes d’erreur d’incompatibilité de réseau MSM.



| Code de raison                                            | Signification                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| \_Code motif \_ WLAN \_ sécurité non prise en charge \_ \_ définie \_ par le \_ système d’exploitation | Les paramètres de sécurité ne sont pas pris en charge par le système d’exploitation. |
| \_Code motif WLAN- \_ \_ jeu de sécurité non pris en charge \_ \_         | Les paramètres de sécurité ne sont pas pris en charge.                         |
| Code motif WLAN non- \_ \_ \_ correspondance du \_ type BSS \_                 | Le type BSS ne correspond pas.                                     |
| Code de motif WLAN sans \_ \_ \_ correspondance de \_ type PHY \_                 | Le type PHY ne correspond pas.                                     |
| réseau de raison WLAN sans correspondance de débit de \_ \_ \_ Vitesse \_                  | Le débit de données ne correspond pas.                                    |



 

Le tableau suivant répertorie les codes d’erreur d’échec de connexion MSM.



| Code de raison                                       | Signification                                                                                                      |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| \_Code motif WLAN annulé par l' \_ \_ utilisateur \_               | L’utilisateur a annulé l’opération.                                                                             |
| échec de l’Association du code de \_ raison WLAN \_ \_ \_          | Pilote déconnecté lors de l’Association.                                                                       |
| \_ \_ \_ \_ délai d’expiration de l’Association du code de raison WLAN          | Expiration du délai d’attente de l’Association.                                                                                       |
| \_échec de \_ la \_ \_ présécurité \_ du code de motif WLAN        | Échec de la sécurité de la pré-Association.                                                                            |
| \_problème de \_ sécurité de démarrage du code de raison WLAN \_ \_ \_      | Échec du démarrage de la sécurité après l’Association.                                                                  |
| \_échec de \_ sécurité du code de motif WLAN \_ \_             | La sécurité se termine avec un échec.                                                                               |
| \_délai de \_ \_ sécurité \_ du code de raison WLAN             | Délai d’expiration de l’opération de sécurité.                                                                                |
| échec de l’itinérance du code de \_ raison WLAN \_ \_ \_              | Pilote déconnecté pendant l’itinérance.                                                                           |
| problème de sécurité de l’itinérance du code de \_ raison WLAN \_ \_ \_ \_    | Échec du démarrage de la sécurité pour l’itinérance.                                                                        |
| \_Code motif WLAN échec de la \_ \_ sécurité ad hoc \_ \_      | Échec du démarrage de la sécurité pour l’homologue ad hoc.                                                                    |
| déconnexion du \_ \_ pilote de code motif \_ WLAN \_          | Pilote déconnecté.                                                                                         |
| échec de l' \_ opération du pilote du code motif WLAN \_ \_ \_ \_    | Le pilote n’a pas réussi à effectuer certaines opérations.                                                                    |
| \_raison WLAN \_ code \_ IHV \_ non \_ disponible           | Le service IHV n’est pas disponible.                                                                            |
| \_raison WLAN \_ code \_ IHV \_ ne \_ répond pas          | La réponse du service IHV a expiré.                                                                 |
| \_ \_ \_ \_ délai d’attente de déconnexion du code de raison WLAN           | Expiration du délai d’attente de la déconnexion du pilote.                                                              |
| \_ \_ erreur interne du code de motif WLAN \_ \_             | Une erreur interne a empêché l’exécution de l’opération.                                              |
| \_ \_ \_ \_ \_ délai d’attente des demandes d’interface utilisateur du code WLAN          | Une demande d’intervention de l’utilisateur a expiré.                                                                        |
| \_Code motif \_ WLAN \_ trop \_ de \_ tentatives de sécurité \_ | Itinérance trop fréquente. La sécurité postérieure n’a pas été effectuée après 5 tentatives.                                         |
| \_Code motif \_ WLAN \_ \_ échec de démarrage AP \_         | Une erreur interne du système d’exploitation s’est produite et a entraîné l’échec du démarrage du réseau hébergé sans fil. |



 

Le tableau suivant répertorie les codes d’erreur de sécurité MSM.



| Code de raison                                                             | Signification                                                                                                                                                                                   |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ index de \_ clé non valide \_                | L’index de clé spécifié n’est pas valide.                                                                                                                                                         |
| \_Code motif \_ WLAN \_ MSMSEC le \_ profil \_ PSK est \_ présent                       | Clé requise, PSK présente.                                                                                                                                                                |
| \_Code motif \_ WLAN \_ \_ longueur de clé de profil MSMSEC \_ \_                        | Longueur de clé non valide.                                                                                                                                                                       |
| \_Code motif WLAN- \_ \_ \_ \_ longueur PSK du profil MSMSEC \_                        | Longueur PSK non valide.                                                                                                                                                                       |
| \_Code motif \_ WLAN \_ MSMSEC \_ profil \_ aucun \_ \_ chiffrement d’authentification \_ spécifié        | Aucune paire authentification/chiffrement n’a été spécifiée.                                                                                                                                                           |
| \_Code de motif WLAN \_ \_ MSMSEC profil de \_ \_ \_ \_ \_ chiffrement d’authentification trop important \_ | Trop de paires d’authentification/de chiffrement spécifiées.                                                                                                                                                     |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ \_ chiffrement d’authentification en double du profil \_            | Le profil contient une paire d’authentification/chiffrement dupliquée.                                                                                                                                              |
| \_Code motif \_ WLAN \_ MSMSEC \_ profil \_ rawData \_ non valide                   | Les données brutes du profil ne sont pas valides.                                                                                                                                                              |
| \_Code motif \_ WLAN \_ MSMSEC \_ le \_ \_ chiffrement d’authentification non valide \_              | Combinaison d’authentification/chiffrement non valide.                                                                                                                                                          |
| \_Code de raison WLAN \_ \_ MSMSEC \_ profil \_ Onex \_ désactivé                     | 802.1 x est désactivé lorsqu’il est nécessaire de l’activer.                                                                                                                                        |
| \_Code de raison WLAN \_ \_ MSMSEC \_ profil \_ Onex \_ activé                      | 802.1 x est activé lorsqu’il doit être désactivé.                                                                                                                                        |
| \_Code motif \_ WLAN \_ MSMSEC \_ profil \_ \_ PMKCACHE \_ mode non valide            | Mode de cache PMK non valide.                                                                                                                                                                   |
| \_raison WLAN \_ code \_ MSMSEC \_ profil de la \_ \_ taille PMKCACHE non valide \_            | Taille du cache PMK non valide.                                                                                                                                                                   |
| \_Code motif \_ WLAN \_ MSMSEC profil de la \_ durée de \_ \_ vie PMKCACHE non valide \_             | TTL du cache PMK non valide.                                                                                                                                                                    |
| \_Code motif \_ WLAN \_ MSMSEC \_ profil \_ d' \_ authentification non \_ valide             | Mode de préauthentification non valide.                                                                                                                                                                     |
| Code motif WLAN MSMSEC profil de la limitation de la pré- \_ \_ \_ \_ \_ authentification non valide \_ \_         | Limitation de la pré-authentification non valide.                                                                                                                                                                 |
| \_Code de raison WLAN MSMSEC profiler la pré- \_ \_ \_ \_ authentification \_ \_ activée uniquement             | Préauthentification activée lorsque le cache PMK est désactivé.                                                                                                                                               |
| \_MSMSEC de motif WLAN \_ \_ \_ réseau de capacité \_                         | La correspondance des fonctionnalités a échoué sur le réseau.                                                                                                                                                    |
| carte réseau raison de la \_ \_ \_ \_ fonctionnalité MSMSEC \_                             | La correspondance des fonctionnalités a échoué au niveau de la carte réseau.                                                                                                                                                        |
| \_profil de motif WLAN \_ \_ MSMSEC \_ profil de capacité \_                         | Échec de la correspondance des fonctionnalités au niveau du profil.                                                                                                                                                    |
| \_détection des \_ \_ fonctionnalités MSMSEC \_ du code de motif WLAN \_                       | Le réseau ne prend pas en charge le type de fonctionnalité spécifié.                                                                                                                                       |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ type phrase secrète \_                   | La phrase secrète contient un caractère non valide.                                                                                                                                                    |
| \_Code motif \_ WLAN \_ MSMSEC du \_ profil \_ \_                  | Le matériel de clé contient un caractère non valide.                                                                                                                                                  |
| \_Code motif \_ WLAN \_ MSMSEC profil de motif \_ \_ incorrect \_                     | Le type de clé spécifié ne correspond pas au matériel de clé.                                                                                                                                   |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ cellule mixte                                 | Une cellule mixte est suspectée. Le point d’accès ne signale pas qu’il est compatible avec un profil de confidentialité.                                                                                  |
| \_Code motif \_ WLAN \_ MSMSEC \_ les \_ minuteurs d’authentification du profil \_ \_ non valides              | Le nombre de minuteries d’authentification ou le nombre de délais d’attente spécifiés dans le profil n’est pas valide.                                                                                        |
| \_Code motif \_ WLAN \_ MSMSEC \_ profil \_ \_ GKEY \_ INTV non valide                | L’intervalle de mise à jour de la clé de groupe spécifié dans le profil n’est pas valide.                                                                                                                        |
| \_Code motif \_ WLAN \_ \_ réseau de transition MSMSEC \_                         | Un « réseau de transition » est soupçonné. La sécurité 802,11 héritée est utilisée pour la prochaine tentative d’authentification.                                                                                  |
| \_Code motif \_ WLAN \_ MSMSEC-clé de \_ Profil non \_ \_ mappée \_                | La clé contient des caractères qui ne sont pas dans le jeu de caractères ASCII.                                                                                                                      |
| \_Code motif \_ WLAN \_ \_ authentification du profil de capacité MSMSEC \_ \_                   | La correspondance des fonctionnalités a échoué, car le réseau ne prend pas en charge la méthode d’authentification dans le profil.                                                                                 |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ chiffrement du profil de capacité \_                 | La correspondance des fonctionnalités a échoué, car le réseau ne prend pas en charge l’algorithme de chiffrement dans le profil.                                                                                      |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ mode sans échec de profil \_                         | La valeur du mode FIPS 140-2 dans le profil n’est pas valide.                                                                                                                                          |
| \_Code de raison WLAN \_ \_ MSMSEC \_ \_ \_ \_ \_ carte réseau en mode sans échec        | Le profil requiert le mode FIPS 140-2, qui n’est pas pris en charge par la carte d’interface réseau (NIC).                                                                                                 |
| Code de raison WLAN MSMSEC de la \_ capacité du \_ profil de \_ \_ capacité \_ \_ \_ en mode sans échec \_ NW         | Le profil requiert le mode FIPS 140-2, qui n’est pas pris en charge par le réseau.                                                                                                                      |
| \_Code motif \_ WLAN \_ MSMSEC \_ profil d' \_ authentification non pris en charge \_                  | Profil spécifie une authentification, un mécanisme non pris en charge.                                                                                                                               |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ chiffrement non pris en charge \_ par le profil                | Profil spécifie un chiffrement non pris en charge.                                                                                                                                                  |
| \_Code motif WLAN échec de la \_ \_ \_ demande d’interface utilisateur MSMSEC \_ \_                        | Échec de la mise en file d’attente de la demande de l’interface utilisateur.                                                                                                                                               |
| \_Code motif \_ WLAN \_ \_ \_ \_ \_ carte réseau MSMSEC Capacity MFP NW                    | Le réseau local sans fil nécessite la protection de trame d’administration (MFP) et l’interface réseau ne prend pas en charge MFP. Pour plus d’informations, consultez l’amendement IEEE 802.11 w vers la norme 802,11. |



 

Le tableau suivant répertorie les codes d’erreur de connexion MSM.



| Code de raison                                             | Signification                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ \_ délai d’attente de démarrage de l’authentification        | l’authentification 802.1 x n’a pas démarré dans le temps imparti.                                                      |
| \_Code motif \_ WLAN \_ \_ \_ \_ délai d’expiration de l’authentification MSMSEC      | l’authentification 802.1 x ne s’est pas terminée dans le temps imparti.                                                   |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ \_ délai d’expiration de la clé de démarrage         | L’échange de clés dynamique n’a pas démarré dans le temps imparti.                                                       |
| \_Code motif \_ WLAN \_ \_ \_ \_ délai d’expiration de la clé MSMSEC       | L’échange de clés dynamique ne s’est pas terminé dans le temps imparti.                                                    |
| \_Code motif \_ WLAN \_ MSMSEC \_ m3 \_ données de clé manquantes \_ \_      | Le message 3 de la négociation à 4 voies n’a pas de données de clé.                                                                    |
| \_Code de raison WLAN \_ \_ MSMSEC \_ m3 manquant dans \_ \_ IE             | Le message 3 de la négociation à 4 voies n’a pas d’IE.                                                                          |
| \_Code motif \_ WLAN \_ MSMSEC \_ m3 \_ clé de GRP manquante \_ \_       | Le message 3 de la négociation à 4 voies n’a pas de clé GRP.                                                                     |
| \_Code motif \_ WLAN \_ MSMSEC \_ \_ correspondance IE \_            | Échec de la correspondance des fonctionnalités de sécurité d’IE dans m3.                                                               |
| \_Code motif \_ WLAN \_ MSMSEC \_ s \_ \_ correspondance IE           | Échec de la correspondance des fonctionnalités de sécurité d’Internet Explorer secondaire dans m3.                                                     |
| \_Code motif \_ WLAN \_ MSMSEC \_ aucune \_ paire de \_ clés           | Clé de paire obligatoire, mais point d’accès configuré uniquement les clés de groupe.                                        |
| \_Code motif WLAN- \_ \_ \_ \_ données de clé manquées MSMSEC G1 \_ \_      | Le message 1 de la négociation de clé de groupe n’a pas de données de clé.                                                                |
| \_Code motif WLAN clé de la \_ \_ \_ \_ GRP manquante MSMSEC G1 \_ \_       | Le message 1 de la négociation de clé de groupe n’a pas de clé de groupe.                                                               |
| \_Code motif \_ WLAN \_ MSMSEC \_ homologue \_ indiqué comme \_ non sécurisé   | Réinitialisation du bit sécurisé sur AP après la sécurisation de la connexion.                                                                |
| \_Code motif \_ WLAN \_ MSMSEC \_ aucun \_ authentificateur           | 802.1 x indique qu’il n’y a pas d’authentificateur, mais le profil en requiert un.                                   |
| \_Code motif WLAN défaillance de la \_ \_ \_ carte réseau MSMSEC \_                | Échec des paramètres de plombation de la carte réseau.                                                                                 |
| \_Code motif \_ WLAN \_ MSMSEC \_ annulé                   | L’opération a été annulée par un appelant.                                                                              |
| FORMAT de la \_ clé du MSMSEC du code de motif WLAN \_ \_ \_ \_                 | Le format de la clé entrée n’est pas valide.                                                                     |
| \_Code motif \_ WLAN \_ MSMSEC \_ rétrogradation \_ détectée         | Une rétrogradation de sécurité a été détectée.                                                                               |
| \_Code motif \_ WLAN \_ MSMSEC \_ clé PSK non \_ correspondante \_ suspectée    | Une incompatibilité de clé PSK est suspectée.                                                                                     |
| \_ \_ \_ \_ échec forcé du code de raison WLAN MSMSEC \_             | Un échec forcé s’est produite, car la méthode de connexion n’était pas sécurisée.                                         |
| \_Code motif \_ WLAN \_ MSMSEC \_ m3 \_ trop \_ nombreux \_ RSNIE        | Le message 3 de la négociation à 4 voies contient un trop grand nombre d’IE RSN (RSN).                                                     |
| \_Code motif \_ WLAN \_ MSMSEC \_ m2 \_ données de clé manquantes \_ \_      | Le message 2 de la négociation à 4 voies n’a pas de données de clé (ad hoc RSN).                                                        |
| \_Code motif \_ WLAN \_ MSMSEC \_ m2 \_ manquant \_ IE             | Le message 2 de la négociation en 4 temps n’a pas d’IE (ad hoc RSN).                                                              |
| \_Code motif \_ WLAN \_ MSMSEC \_ auth \_ WCN \_ terminée        |                                                                                                                  |
| \_Code motif \_ WLAN \_ \_ échec de \_ l’interface utilisateur de sécurité MSMSEC \_       | La demande d’interface utilisateur de sécurité a échoué, car la demande n’a pas pu être mise en file d’attente ou parce que l’utilisateur a annulé la demande. |
| \_Code motif \_ WLAN \_ MSMSEC m3 code de \_ \_ \_ gestion manquant \_ \_ clé de la GRP | Le message 3 de la négociation à 4 voies n’a pas de clé de groupe de gestion (RSN).                                                        |
| \_Code motif WLAN clé de la \_ \_ \_ GRP de gestion MSMSEC G1 \_ manquant \_ \_ \_ | Le message 1 de la négociation de clé de groupe n’a pas de clé de gestion de groupe.                                                    |



 

Le tableau suivant répertorie les codes de raison 802.1 X. Les éléments de schéma nommés ci-dessous sont définis dans le schéma OneX et sont spécifiés dans le profil WLAN.



| Code de raison                                         | Signification                                                                                                                                                                            |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ONEX \_ ne peut pas \_ \_ identifier l' \_ utilisateur                    | Aucun utilisateur n’est disponible pour l’authentification 802.1 X. Cette erreur peut se produire lorsque l’authentification de l’ordinateur est désactivée et qu’aucun utilisateur n’a ouvert de session sur l’ordinateur.                              |
| \_identité Onex \_ \_ introuvable                          | L’identité 802.1 X est introuvable.                                                                                                                                            |
| \_IU Onex \_ désactivée                                  | L’authentification ne peut être effectuée que par le biais de l’interface utilisateur et cette interface n’a pas pu être affichée.                                                                       |
| \_échec EAP \_ Onex \_ reçu                        | L’authentification EAP a échoué.                                                                                                                                                     |
| l' \_ AUTHENTIFICATEUR Onex \_ n' \_ est plus \_ présent            | L’authentificateur 802.1 X s’est éloigné du réseau.                                                                                                                               |
| \_version de profil Onex \_ \_ non \_ prise en charge              | La version du profil OneX fournie n’est pas prise en charge.                                                                                                                         |
| \_longueur du profil Onex \_ non valide \_                      | La longueur du profil OneX n’est pas valide.                                                                                                                                            |
| \_ \_ type EAP non autorisé du profil Onex \_ \_                | Le type EAP spécifié dans le profil OneX (éventuellement fourni par l’élément EAPType) n’est pas autorisé.                                                                               |
| \_ \_ \_ \_ type \_ ou \_ indicateur EAP non valide pour le profil Onex         | Le type EAP spécifié dans le profil OneX (éventuellement fourni par l’élément EAPType) n’est pas valide ou l’un des indicateurs EAP (éventuellement fourni dans l’élément EAPConfig) n’est pas valide. |
| \_ \_ indicateurs Onex non valides du profil Onex \_ \_                 | Les indicateurs du demandeur (éventuellement fournis dans l’élément EAPConfig) dans le profil OneX ne sont pas valides.                                                                                 |
| \_ \_ \_ valeur du minuteur du profil Onex non valide \_                | Un minuteur spécifié dans le profil OneX (éventuellement fourni par l’élément heldPeriod, authPeriod ou startPeriod) n’est pas valide.                                                        |
| \_Profil Onex \_ \_ mode demandeur non valide \_            | Le mode demandeur spécifié dans le profil OneX (éventuellement fourni par l’élément supplicantMode) n’est pas valide.                                                                    |
| \_mode d' \_ authentification non valide du profil \_ Onex \_                  | Le mode d’authentification spécifié dans le profil OneX (éventuellement fourni par l’élément authMode) n’est pas valide.                                                                      |
| \_Propriétés de \_ \_ connexion EAP \_ non valide du profil Onex \_ | Les propriétés de connexion spécifiées dans le profil OneX (éventuellement fourni par l’élément EAPConfig) ne sont pas valides.                                                                  |



 

## <a name="remarks"></a>Remarques

un ensemble limité de codes de raison est pris en charge sur Windows xp avec service pack 3 (SP3) et sur l’API de réseau local sans fil pour Windows XP avec service pack 2 (SP2). les codes d’erreur de validation de profil pris en charge sur Windows xp avec SP3 et sur l’API de réseau local sans fil pour Windows XP avec SP2 sont les suivants :

-   \_Code motif WLAN- \_ \_ schéma de profil non valide \_ \_
-   \_Profil du motif WLAN \_ \_ \_ manquant
-   \_SSID du profil de motif WLAN \_ \_ \_ \_ non valide

les codes d’erreur de sécurité MSM pris en charge sur Windows xp avec SP3 et sur l’API de réseau local sans fil pour Windows XP avec SP2 sont les suivants :

-   \_Code motif \_ WLAN \_ MSMSEC \_ \_ index de \_ clé non valide \_
-   \_Code motif \_ WLAN \_ \_ longueur de clé de profil MSMSEC \_ \_
-   \_Code motif WLAN- \_ \_ \_ \_ longueur PSK du profil MSMSEC \_
-   \_Code motif \_ WLAN \_ MSMSEC \_ le \_ \_ chiffrement d’authentification non valide \_
-   \_Code de raison WLAN \_ \_ MSMSEC \_ profil \_ Onex \_ désactivé
-   \_Code de raison WLAN \_ \_ MSMSEC \_ profil \_ Onex \_ activé
-   \_MSMSEC de motif WLAN \_ \_ \_ réseau de capacité \_
-   carte réseau raison de la \_ \_ \_ \_ fonctionnalité MSMSEC \_
-   \_Code motif \_ WLAN \_ MSMSEC du \_ profil \_ \_
-   \_Code motif \_ WLAN \_ MSMSEC profil de motif \_ \_ incorrect \_

les codes d’erreur 802.1 x pris en charge sur Windows xp avec SP3 et sur l’API de réseau local sans fil pour Windows XP avec SP2 sont les suivants :

-   \_longueur du profil Onex \_ non valide \_
-   \_ \_ \_ \_ type \_ ou \_ indicateur EAP non valide pour le profil Onex
-   \_mode d' \_ authentification non valide du profil \_ Onex \_
-   \_Propriétés de \_ \_ connexion EAP \_ non valide du profil Onex \_

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/>                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wlanapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
</dt> <dt>

[**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
</dt> </dl>

 

 
