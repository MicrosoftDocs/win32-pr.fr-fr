---
description: Le Microsoft Digest Challenge est généré par l’appel initial du serveur à la fonction AcceptSecurityContext (Digest).
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Génération de la demande de condensé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a01a7edfa6498ed621e351c114e65a6d4ff6ef7a75b459cb29e00f0dc668a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623329"
---
# <a name="generating-the-digest-challenge"></a>Génération de la demande de condensé

Le Microsoft Digest Challenge est généré par l’appel initial du serveur à la fonction [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Cet appel de fonction génère un nonce, qui est une valeur unique qui contient des informations qui peuvent être utilisées pour détecter des violations de sécurité. Cet appel génère également un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) partiel qui est utilisé pour conserver les informations d’État. Lors de l’appel de **AcceptSecurityContext (Digest)** , vous spécifiez des indicateurs de contexte pour contrôler le comportement de Microsoft Digest et pour définir la qualité de la protection. Pour plus d’informations, consultez [Configuration requise du contexte de test Digest](#digest-challenge-context-requirements).

La sortie de l’appel initial à la [*fonction*](/windows/desktop/SecGloss/c-gly) [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) est un tampon de sécurité qui contient un jeton envoyé au client avec une réponse HTTP 401 (accès refusé).

> [!Note]  
> Les appels à [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) qui ne contiennent pas d’informations dans les tampons d’entrée retournent une stimulation Digest.

 

## <a name="digest-challenge-context-requirements"></a>Exigences du contexte de Challenge Digest

Les spécifications de contexte sont des indicateurs qui déterminent :

-   Indique si Microsoft Digest fonctionne comme un mécanisme SASL ou un protocole d’authentification HTTP.
-   Qualité de protection prise en charge par le contexte de sécurité partagé par le client et le serveur.

Par défaut, Microsoft Digest fonctionne comme un mécanisme SASL. Pour l’utiliser pour l’authentification HTTP, l' \_ indicateur ASC req \_ http (0x10000000) doit être défini par le serveur.

Les spécifications de contexte sont spécifiées sous la forme d’indicateurs transmis au paramètre *fContextReq* de la fonction [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Les indicateurs affectent la qualité de protection du contexte de sécurité en contrôlant la directive QoP dans le défi.

Par défaut, la directive QoP a la valeur « auth ». Pour générer une stimulation qui définit la directive QoP sur « auth-int », le serveur doit spécifier un ou plusieurs des indicateurs suivants :

-   \_intégrité des demandes ASC \_
-   détection de la \_ RElecture de la demande ASC \_ \_
-   détection de la \_ séquence de demande ASC \_ \_

Pour SASL uniquement : générez un Challenge avec la directive QoP définie sur « auth-conf » en spécifiant \_ l' \_ indicateur ASC requirer Context requirement. Comme cet indicateur n’est pas valide pour l’authentification HTTP, il ne peut pas être utilisé avec l' \_ \_ indicateur http ASC req.

Pour plus d’informations sur la directive QoP, consultez [qualité de protection et chiffrements](quality-of-protection-and-ciphers.md).

Pour plus d’informations sur les défis, consultez [contenu d’une demande de résumé](contents-of-a-digest-challenge.md).

 

 
