---
description: Utilisation du protocole COPP (Certified Output Protection Protocol)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Utilisation du protocole COPP (Certified Output Protection Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c97ee1daf62f2d1fb42cdb63e02ae31991c168cfeaaf4437c2e77643fc6cbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086769"
---
# <a name="using-certified-output-protection-protocol-copp"></a>Utilisation du protocole COPP (Certified Output Protection Protocol)

Le protocole COPP (Certified Output Protection Protocol) permet à une application de protéger un flux vidéo lorsqu’il passe de la carte graphique au périphérique d’affichage. Une application peut utiliser COPP pour découvrir le type de connecteur physique attaché au périphérique d’affichage, ainsi que les types de protection de sortie disponibles. Les mécanismes de protection sont les suivants :

-   High-Bandwidth protection du contenu numérique (HDCP)
-   Système de gestion de la génération de copie — analogique (CGMS-A)
-   Protection contre la copie analogique (ACP)

Si la carte graphique prend en charge l’un de ces mécanismes, l’application peut utiliser COPP pour définir le niveau de protection.

COPP définit un protocole qui est utilisé pour établir un canal de communication sécurisé avec le pilote Graphics. Il utilise des codes d’authentification de message (Mac) pour vérifier l’intégrité des commandes COPP transmises entre l’application et le pilote d’affichage. l’application utilise COPP en appelant des méthodes sur l’interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) du filtre de convertisseur de mixage vidéo DirectShow (vmr-7 ou vmr-9).

COPP ne définit rien sur les stratégies de droits numériques qui peuvent s’appliquer au contenu multimédia numérique. En outre, COPP n’implémente aucun système de protection de sortie. Le protocole COPP permet simplement de définir et d’interroger des niveaux de protection sur la carte graphique, à l’aide des systèmes de protection fournis par l’adaptateur.

Cette section suppose que vous êtes familiarisé avec les technologies suivantes :

-   DirectShow
-   Windows Media Format SDK
-   XML
-   Chiffrement à clé publique et chiffrement symétrique

Les exemples de code de cette section utilisent le CryptoAPI de Microsoft pour effectuer des opérations de chiffrement. Cette section contient les rubriques suivantes :

-   [Vue d’ensemble de COPP](overview-of-copp.md)
-   [Obtention de la chaîne de certificats du pilote](obtaining-the-drivers-certificate-chain.md)
-   [Validation de la chaîne de certificats](validating-the-certificate-chain.md)
-   [Listes de révocation de certificats](certificate-revocation-lists.md)
-   [Importation de la clé publique du pilote](importing-the-drivers-public-key.md)
-   [Lancement d’une session COPP](initiating-a-copp-session.md)
-   [Envoi de demandes d’État COPP](sending-copp-status-requests.md)
-   [Envoi de commandes COPP](sending-copp-commands.md)
-   [Tester si un pilote graphique prend en charge COPP](testing-whether-a-graphics-driver-supports-copp.md)
-   [Informations de référence sur les requêtes COPP](copp-query-reference.md)
-   [Informations de référence sur les commandes COPP](copp-command-reference.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du convertisseur de mixage vidéo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



