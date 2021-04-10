---
description: Les clouds sont utilisés par les infrastructures de regroupement et de représentation graphique des homologues.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Clouds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115579"
---
# <a name="clouds"></a>Clouds

Les clouds sont utilisés par les infrastructures de [regroupement](grouping-api.md) et de [représentation graphique](graphing-api.md) des homologues. Le [protocole PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) identifie un Cloud comme un ensemble d’homologues qui peuvent communiquer au sein de la même étendue IPv6. Les clouds sont étroitement liés aux étendues IPv6. La liste suivante répertorie certaines des fonctionnalités de Cloud uniques :

-   Un Cloud est identifié par un nom, et les clouds disponibles peuvent être énumérés à l’aide de [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).
-   Si un ordinateur est connecté à Internet, il fait partie d’un Cloud global, qui est identifié par la chaîne « global \_ ».
-   Si un ordinateur est connecté à un ou plusieurs réseaux locaux (LAN), des clouds individuels sont disponibles pour chaque lien.
-   Un ordinateur peut être connecté à plusieurs réseaux à l’aide de plusieurs cartes réseau ou à l’aide d’un réseau privé virtuel (VPN), ce qui signifie qu’un ordinateur avec une interface peut être visible dans de nombreux Clouds.
-   Vous pouvez utiliser PNRP pour inscrire et résoudre des noms d’homologue dans un Cloud spécifique.

 

 



