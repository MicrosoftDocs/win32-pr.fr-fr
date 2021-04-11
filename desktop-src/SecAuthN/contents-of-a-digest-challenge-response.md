---
description: Le client doit envoyer une réponse de stimulation de synthèse au serveur lorsqu’il reçoit une demande de synthèse en réponse à une demande de ressource.
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: Contenu d’une réponse de stimulation Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203377"
---
# <a name="contents-of-a-digest-challenge-response"></a>Contenu d’une réponse de stimulation Digest

Le client doit envoyer une réponse de stimulation de synthèse au serveur lorsqu’il reçoit une demande de synthèse en réponse à une demande de ressource. Le client doit renvoyer la demande, en fournissant un en-tête d’autorisation avec la réponse de stimulation. Le tableau suivant décrit les directives qui composent une réponse de test Digest.



| Directive          | Description                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | Nom de compte du [*principal de sécurité*](/windows/desktop/SecGloss/s-gly) qui demande la ressource.                                                                  |
| Realm              | Nom du domaine qui contient le compte indiqué par le nom d’utilisateur.                                                                                                                                                    |
| nonce              | Valeur à usage unique reçue dans le test Digest.                                                                                                                                                                                |
| URI                | URI (Universal Resource Identifier) de la ressource demandée.                                                                                                                                                         |
| qop                | [Qualité de la protection](quality-of-protection.md).                                                                                                                                                                    |
| obten                 | Nombre de valeur unique. Nombre de fois où le client a envoyé une réponse à une demande de vérification à l’aide de la valeur à usage unique. Pour plus d’informations, consultez la directive nonce.                                                                              |
| cnonce             | Valeur encodée unique générée par le client pour chaque réponse de stimulation.                                                                                                                                                |
| réponse           | Valeur calculée en fonction de la spécification d’accès Digest ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)). Une réponse exacte est une preuve concluante que le mot de passe de l’utilisateur est connu côté client. |
| algorithme          | L’algorithme reçu dans le test Digest.                                                                                                                                                                            |
| manière             | Valeur opaque reçue dans le test Digest.                                                                                                                                                                         |
| (SASL uniquement) chiffrement | L’une des valeurs de chiffrement reçues dans le test Digest. Pour plus d’informations sur le chiffrement, consultez [qualité de protection et chiffrements](quality-of-protection-and-ciphers.md).                                                             |



 

Microsoft Digest prend en charge les formes de nom d’utilisateur/domaine suivantes :

-   Domaine du nom d’utilisateur
-   Domaine AccountName (plat)
-   UPN "" (vide)
-   NetBIOS "" (vide)

Si les caractères majuscules sont pris en charge, pour des performances optimales correspondant aux valeurs de hachage précalculées précalculées du serveur, il est recommandé d’utiliser des caractères minuscules.

L’utilisation de hachages précalculés est une nouvelle fonctionnalité qui permet aux opérateurs système d’ignorer l’utilisation de mots de passe chiffrés réversibles sur le contrôleur de domaine. Un hachage précalculé est formé pour un utilisateur lorsque le mot de passe de l’utilisateur est modifié.

Microsoft Digest génère la chaîne de réponse de test Digest pour les applications clientes. Pour plus d’informations, consultez [génération de la réponse aux demandes de test Digest](generating-the-digest-challenge-response.md).

 

 
