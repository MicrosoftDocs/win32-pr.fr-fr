---
description: Les informations d’identification de l’utilisateur sont requises par Microsoft Digest ; le client et le serveur doivent présenter des informations d’identification valides pour pouvoir établir un contexte de sécurité pour l’échange de messages. Les handles d’informations d’identification sont utilisés pour obtenir et présenter les informations d’identification.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtention d’informations d’identification SSP Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484712"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>Obtention d’informations d’identification SSP Microsoft Digest

Les [*informations d’identification*](../secgloss/c-gly.md) de l’utilisateur sont requises par Microsoft Digest ; le client et le serveur doivent présenter des informations d’identification valides pour pouvoir établir un [*contexte de sécurité*](../secgloss/s-gly.md) pour l’échange de messages. Les handles d’informations d’identification sont utilisés pour obtenir et présenter les informations d’identification.

Étant donné que le handle d’informations d’identification est utilisé pour stocker les informations de configuration, le même handle ne peut pas être utilisé pour les opérations côté client et côté serveur. Cela signifie que les applications qui prennent en charge les connexions client et serveur doivent obtenir au moins deux handles d’informations d’identification.

Pour obtenir un descripteur des informations d’identification requises par Microsoft Digest, appelez la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .

Les exemples de langage C suivants montrent comment obtenir des informations d’identification.

-   [Obtention des informations d’identification Digest par défaut](obtaining-default-digest-credentials.md)
-   [Obtention d’autres informations d’identification de Digest](obtaining-alternate-digest-credentials.md)

 

 
