---
description: Après avoir reçu un défi du serveur, le client crée la réponse de la stimulation de synthèse en appelant la fonction InitializeSecurityContext (Digest).
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: Génération de la réponse de test Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5e763591294eb14fce6ac79225bbe24ba40bc875ab731c986a694df956ee356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101299"
---
# <a name="generating-the-digest-challenge-response"></a>Génération de la réponse de test Digest

Après avoir reçu un défi du serveur, le client crée la réponse de la stimulation de synthèse en appelant la fonction [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Cette fonction génère une empreinte digitale de [*hachage*](/windows/desktop/SecGloss/h-gly) MD5 en utilisant des informations sur la ressource demandée et les données de la demande, et génère un jeton de sécurité qui représente un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly)partiel. Pour terminer l’authentification, le client doit retourner le jeton au serveur qui a émis la demande.

Le tableau suivant décrit les paramètres de la [*fonction*](/windows/desktop/SecGloss/c-gly) [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) et les valeurs à fournir lors de la création d’une réponse à une demande de test Digest.



| Paramètre                  | Description                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fContextReq*<br/>   | Attributs de contexte de sécurité demandés par le client. Pour plus d’informations, consultez Configuration requise du contexte de la réponse de test Digest.<br/>                                                             |
| *pszTargetName*<br/> | HTTP : chaîne terminée par le caractère null qui spécifie l’URL cible.<br/> SASL : chaîne terminée par le caractère null qui spécifie la cible DNS/SPN.<br/>                                                         |
| *pInput*<br/>        | Mémoires tampons qui contiennent des informations requises par le SSP Digest. Pour plus d’informations, consultez [mémoires tampons d’entrée pour la réponse à la demande Digest](input-buffers-for-the-digest-challenge-response.md).<br/> |
| *pfContextAttr*<br/> | Reçoit les attributs pris en charge par le contexte de sécurité retourné. Pour plus d’informations, consultez Configuration requise du contexte de la réponse de test Digest.<br/>                                                  |
| *pOutput*<br/>       | Adresse d’une \_ mémoire tampon de type de jeton SECBUFFER qui reçoit un jeton de sécurité à renvoyer au serveur.<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>Exigences du contexte de réponse de stimulation Digest

Les spécifications de contexte sont des indicateurs qui déterminent :

-   Indique si Microsoft Digest fonctionne comme un mécanisme SASL ou un protocole d’authentification HTTP.
-   Qualité de protection prise en charge par le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) partagé par le client et le serveur.

Par défaut, Microsoft Digest fonctionne comme un mécanisme SASL.

Les spécifications de contexte sont spécifiées sous la forme d’indicateurs passés au paramètre *fContextReq* de la fonction [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Les indicateurs affectent la qualité de protection du contexte de sécurité en contrôlant la directive QoP dans la réponse de stimulation.

Par défaut, la directive QoP a la valeur « auth ». Pour générer une réponse de stimulation qui affecte à QoP la valeur « auth-int », les conditions suivantes doivent être remplies :

1.  La vérification Digest doit avoir une directive QoP définie sur « auth-int ».
2.  Le client doit spécifier un ou plusieurs des indicateurs suivants :

    -   intégrité de la \_ demande ISC \_
    -   \_détection de \_ relecture de la demande ISC \_
    -   \_détection de \_ séquence de demande ISC \_

Pour SASL uniquement : génère une réponse de stimulation avec la directive QoP définie sur « auth-conf » en spécifiant l' \_ indicateur de confidentialité des demandes ISC \_ . Comme cet indicateur n’est pas valide pour l’authentification HTTP, il ne peut pas être utilisé avec l' \_ \_ indicateur http ISC req.

## <a name="verifying-the-quality-of-protection"></a>Vérification de la qualité de la protection

Le client doit examiner les indicateurs d’attributs de contexte de sécurité retournés dans le paramètre *pfContextAttr* de la fonction [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Le client doit envoyer la réponse de stimulation au serveur uniquement si la qualité de protection indiquée par les indicateurs est suffisante pour ses besoins. Les indicateurs pertinents peuvent être n’importe quelle combinaison des éléments suivants :

-   intégrité d’ISC \_ RET \_
-   \_détection de \_ relecture ISC RET \_
-   détection de la \_ séquence ISC RET \_ \_
-   \_ \_ Confidentialité de la confidentialité d’ISC (contextes SASL uniquement)

Pour plus d’informations sur la directive QoP, consultez [qualité de protection et chiffrements](quality-of-protection-and-ciphers.md).

Pour plus d’informations sur les directives de réponse aux stimulations, consultez [le contenu d’une réponse de test Digest](contents-of-a-digest-challenge-response.md).

 

