---
description: Vue d’ensemble de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Vue d’ensemble de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514311"
---
# <a name="overview-of-copp"></a>Vue d’ensemble de COPP

Voici les étapes de base qu’une application doit effectuer pour utiliser le protocole COPP (Certified Output Protection Protocol).

**Récupérer la chaîne de certificats du pilote**

1.  Générez un graphique de lecture DirectShow qui affiche la vidéo à l’aide du convertisseur de mixage vidéo (VMR-7 ou VMR-9) ou du filtre de [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR).
2.  Interrogez VMR pour obtenir l’interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .
3.  Appelez [**IAMCertifiedOutputProtection :: KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Cette méthode retourne un nombre aléatoire 128 bits du pilote, ainsi qu’une chaîne de certificats qui contient la clé publique RSA 2048 bits du pilote.

**Valider la chaîne de certificats**

1.  Validez la chaîne de certificats. Si la chaîne de certificats n’est pas valide, arrêtez.
2.  Vérifiez la liste de révocation de certificats (CRL). Si l’un des certificats de la chaîne de certificats apparaît dans la liste de révocation, arrêtez.
3.  Récupération de la clé publique RSA à partir de la chaîne de certificats.

**Initialiser la session COPP**

1.  Générez une clé de session AES 128 bits. Cette clé est utilisée pour signer des données et vérifier que les données signées n’ont pas été falsifiées.
2.  Générer deux nombres aléatoires 32 bits sécurisés par chiffrement. Le premier est un numéro de séquence d’État, tandis que le second est un numéro de séquence de commande. Chaque fois que l’application envoie une commande ou une demande d’État, elle incrémente le numéro de séquence correspondant et y ajoute ce numéro dans la commande COPP ou les données de la requête.
3.  Concaténez le nombre aléatoire 128 bits à partir du pilote Graphics, la clé de session AES, le numéro de séquence d’État et le numéro de séquence de commande. Chiffrez ce tableau d’octets à l’aide de la clé publique du pilote et transmettez le résultat à [**IAMCertifiedOutputProtection :: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).

**Envoyer des commandes et des requêtes d’État COPP**

1.  Interrogez les types de protection disponibles et d’autres informations en appelant [**IAMCertifiedOutputProtection ::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).
2.  Définissez les niveaux de protection souhaités en appelant [**IAMCertifiedOutputProtection ::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).
3.  Interrogez régulièrement le niveau de protection local actuel. Arrêter la lecture si le niveau de protection local change de façon inattendue ou si un problème est détecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



