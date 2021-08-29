---
description: La documentation suivante est valide uniquement lorsque Digest est utilisé en tant que mécanisme SASL. Les chiffrements et le chiffrement ne sont pas disponibles pour l’authentification HTTP à l’aide de Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Chiffrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d406b610964cb07e88295c472d89a600586308d482f02e7f04633f2a01be6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883509"
---
# <a name="ciphers"></a>Chiffrements

La documentation suivante est valide uniquement lorsque Digest est utilisé en tant que mécanisme SASL. Les chiffrements et le chiffrement ne sont pas disponibles pour l’authentification HTTP à l’aide de Microsoft Digest.

La directive de chiffrement d’un challenge SASL Digest contient une liste des chiffrements pris en charge par un serveur nécessitant des communications confidentielles. La directive de chiffrement ne peut être incluse que si la directive QoP a la valeur « auth-CONF ». Les chiffrements reconnus par Microsoft Digest sont répertoriés dans le tableau suivant, dans l’ordre, de la plus forte à la plus faible.



| Valeur de chiffrement | Description                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RC4        | Le chiffrement RC4 avec une clé de 128 bits.                                                                                                                                                                                                                                                             |
| alors       | Le chiffrement [*triple des*](/windows/desktop/SecGloss/t-gly) en mode [*CBC*](/windows/desktop/SecGloss/c-gly) avec Ede avec la même clé pour chaque étape E (mode à deux clés). La longueur totale de la clé est de 112 bits. |
| « RC4-56 »     | Le chiffrement RC4 avec une clé de 56 bits.                                                                                                                                                                                                                                                              |
| « RC4-40 »     | Le chiffrement RC4 avec une clé de 40 bits.                                                                                                                                                                                                                                                              |
| des        | Le chiffrement des ( [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) ) dans le mode de [*chaînage de blocs de chiffrement*](/windows/desktop/SecGloss/c-gly) (CBC) avec une clé de 56 bits. |



 

Quand une application serveur demande la confidentialité (QoP = "auth-conf") Microsoft Digest génère une stimulation qui offre au client tous les chiffrements installés sur le serveur et pris en charge par le Digest. Le client Digest sélectionne le chiffrement le plus élevé disponible. Pour plus d’informations sur la spécification de la confidentialité, consultez [génération de la demande de résumé](generating-the-digest-challenge.md).

 

 
