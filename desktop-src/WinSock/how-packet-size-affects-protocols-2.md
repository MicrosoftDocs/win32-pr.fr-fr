---
description: Les problèmes liés à la taille des paquets multimédias décrits dans la rubrique, à propos de la taille des paquets multimédias, affectent différemment les différents \_ protocoles IPX de PF.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Impact de la taille des paquets sur les protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa654e8884f56ae8079375fa32764ad240f0c870229d07e50623f6e18e42958b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051637"
---
# <a name="how-packet-size-affects-protocols"></a>Impact de la taille des paquets sur les protocoles

Les problèmes liés à la taille des paquets multimédias décrits dans la rubrique, [à propos de la taille des paquets multimédias](about-media-packet-size-2.md), affectent différemment les différents \_ protocoles IPX de PF. Une stratégie courante pour gérer les différentes contraintes de taille de routeur et de média consiste à utiliser la taille de média complète lorsque le numéro de réseau de la station distante correspond à la station locale, et à revenir à la taille de paquet minimale, dans le cas contraire.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>\_IPX NSPROTO
</dt> <dd>

Fournit un service de datagrammes ; chaque datagramme doit résider dans la taille de paquet maximale. Winsock définit la taille maximale des paquets de datagrammes sur la taille du paquet de média local moins l’en-tête IPX. Gardez toutefois à l’esprit que si le paquet est routé, il peut atteindre des restrictions de routeur en cours d’acheminement. Assurez-vous que votre application peut revenir à des datagrammes de 546 octets.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

Fournit des services de flux et de paquets séquencés. Winsock IPX/SPX permet aux flux de données et aux messages d’être répartis sur plusieurs paquets. par conséquent, la taille des paquets ne limite pas la quantité de données gérées par l' [**envoi**](/windows/desktop/api/Winsock2/nf-winsock2-send) et la [**réception**](/windows/desktop/api/winsock/nf-winsock-recv). Toutefois, la taille du média sous-jacent doit être définie correctement ou le premier paquet volumineux sera non remis et la connexion sera réinitialisée. Si la station cible se trouve sur le réseau local, Winsock définit sa taille de paquet sur la taille du paquet multimédia. Dans le cas contraire, la valeur par défaut est de 512 octets. Cette taille peut être modifiée immédiatement après la [**connexion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou l' [**acceptation**](/windows/desktop/api/Winsock2/nf-winsock2-accept) via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

SPXII comprend une grande négociation de paquets Internet pour maintenir une taille optimale pour les paquets et ne nécessite pas d’intervention du programmeur. Toutefois, si la station à distance ne prend pas en charge SPXII et négocie avec la norme SPX standard, les \_ règles NSPROTO SPX sont activées.



| Protocol     | Média      | Type        | Taille des paquets de données |
|--------------|------------|-------------|------------------|
| \_IPX NSPROTO | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | Snapshots        |                  |
|              | Token ring | 4 mégabits   |                  |
|              |            | 16 mégabits  |                  |
| NSPROTO \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | Snapshots        |                  |
|              | Token ring | 4 mégabits   |                  |
|              |            | 16 mégabits  |                  |



 

</dd> </dl>

 

 



