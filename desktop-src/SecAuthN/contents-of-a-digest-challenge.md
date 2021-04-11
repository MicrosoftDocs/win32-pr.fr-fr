---
description: La taille d’une demande d’accès Digest doit être inférieure à 2048 octets.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenu d’une demande de résumé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112199"
---
# <a name="contents-of-a-digest-challenge"></a>Contenu d’une demande de résumé

La taille d’une demande d’accès Digest doit être inférieure à 2048 octets. L’exemple suivant montre une stimulation assignée à la chaîne de caractères szChallenge.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> La chaîne de stimulation est placée entre guillemets doubles et contient des guillemets doubles incorporés. Les guillemets doubles incorporés doivent être précédés d’une barre oblique inverse ( \\ ).

 

Un challenge Digest peut contenir les directives suivantes.



| Directive         | Description                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| realm             | Indicateur défini par l’implémentation au client sur lequel les [*informations d’identification*](/windows/desktop/SecGloss/c-gly) sont requises. Le client doit afficher ces informations à l’utilisateur s’il demande des informations d’identification.                                                  |
| algorithme         | Microsoft Digest prend en charge MD5 et MD5-sess. Pour des performances optimales, utilisez MD5-sess.                                                                                                                                                                                                                     |
| qop               | Cette directive peut être définie sur auth, auth-int ou auth-CONF. Pour plus d’informations, consultez [qualité de la protection et des chiffrements](quality-of-protection-and-ciphers.md).                                                                                                                                       |
| nonce             | Valeur encodée unique générée par le serveur pour chaque stimulation. Cette valeur ne doit pas être modifiée par le client.                                                                                                                                                                                       |
| manière            | Contient une référence pour le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) en cours d’établissement. Pour plus d’informations, consultez [maintenance du contexte de sécurité entre les connexions](maintaining-the-security-context-between-connections.md). |
| chiffrement (SASL uniquement) | Liste des chiffrements pris en charge par le serveur. Cet élément peut être présent dans un challenge SASL Digest uniquement si la directive QoP spécifie auth-CONF. Pour plus d’informations, consultez [qualité de la protection et des chiffrements](quality-of-protection-and-ciphers.md).                                              |
| charset           | Cette directive peut être définie sur UTF-8 Si le serveur peut traiter les noms d’utilisateur et les domaines encodés en UTF-8. Si le client comprend la directive CharSet, il peut répondre en utilisant des valeurs encodées en UTF-8.                                                                                                       |



 

Microsoft Digest génère la chaîne de Challenge Digest pour les applications serveur. Pour plus d’informations, consultez [génération de la demande de résumé](generating-the-digest-challenge.md).

 

 
