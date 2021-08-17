---
description: La qualité de protection, identifiée par la directive QoP, est d’abord spécifiée par le serveur dans le test Digest, puis confirmée par le client dans la réponse de la stimulation.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Qualité de la protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202acbf319601af74efc35117990f27cc6edff76f27da243453f82bf50984977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920448"
---
# <a name="quality-of-protection"></a>Qualité de la protection

La qualité de protection, identifiée par la directive QoP, est d’abord spécifiée par le serveur dans le test Digest, puis confirmée par le client dans la réponse de la stimulation. Si le client requiert une qualité de protection que le serveur ne prend pas en charge, le client doit mettre fin à l’authentification.

Les valeurs possibles pour la directive QoP sont décrites dans le tableau suivant.



| Valeur                   | Description                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| authentifié                  | Authentification uniquement.                                                                                                                         |
| « AUTH-int »              | Authentification et vérification de l' [*intégrité*](../secgloss/i-gly.md) à l’aide de signatures.                  |
| (SASL uniquement) « AUTH-CONF » | Vérification de l’authentification, de l’intégrité et de la confidentialité à l’aide des signatures et du chiffrement. Pour plus d’informations, consultez la page [chiffrements](ciphers.md). |



 

La qualité de la protection est déterminée par les indicateurs de spécifications de contexte passés au SSP Microsoft Digest. Le tableau suivant répertorie les indicateurs relatifs à la qualité de protection et la valeur résultante de la directive QoP.



| Indicateur                         | valeur QoP               |
|------------------------------|-------------------------|
| *Xxx* \_ confidentialité des demandes \_  | « AUTH-conf » (SASL uniquement) |
| *Xxx* \_ détection de la \_ RElecture de la demande \_   | « AUTH-int »              |
| *Xxx* \_ \_détection de séquence de demande \_ | « AUTH-int »              |
| *Xxx* \_ intégrité de la demande \_        | « AUTH-int »              |
| (aucun)                       | authentifié                  |



 

> [!Note]  
> Les indicateurs d’exigence de contexte spécifiés par les applications serveur ont un préfixe ASC, et ceux spécifiés par les clients sont préfixés par ISC. Pour déterminer les valeurs d’indicateur utilisées par votre application, remplacez l’un de ces préfixes par *xxx*.

 

Pour obtenir des informations supplémentaires sur le serveur, consultez [génération de la demande de résumé](generating-the-digest-challenge.md).

Pour obtenir des informations supplémentaires sur le client, consultez [génération de la réponse](generating-the-digest-challenge-response.md)aux demandes de test Digest.

 

 
