---
description: Dans une infrastructure à clé publique Microsoft, les demandes de certificat sont envoyées à partir d’ordinateurs clients vers des autorités de certification en tant que chaîne binaire qui contient une séquence de structures de données encodées.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Encodage de demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756544"
---
# <a name="certificate-request-encoding"></a>Encodage de demande de certificat

Dans une infrastructure à clé publique Microsoft, les demandes de certificat sont envoyées à partir d’ordinateurs clients vers des autorités de certification en tant que chaîne binaire qui contient une séquence de structures de données encodées. L’API d’inscription de certificats utilise le ASN. 1 (Abstract Syntax Notation One) pour décrire et encoder ces structures. Dans le cadre de cette documentation, ASN. 1 peut être divisé de manière conceptuelle en règles syntaxiques (ISO 8824) qui décrivent les structures de données et les règles d’encodage (ISO 8825) qui spécifient la façon dont les données doivent être encodées pour la transmission réseau. Pour plus d'informations, voir les rubriques suivantes :

-   [Présentation de la syntaxe et de l’encodage ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [Système de type ASN. 1](about-asn-1-type-system.md)
-   [Distinguished Encoding Rules](distinguished-encoding-rules.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



