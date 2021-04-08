---
description: L’opération de blocage permet à une seule adresse de gérer plusieurs sessions de communication.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Mise en attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863230"
---
# <a name="hold"></a>Mise en attente

L’opération de blocage permet à une seule adresse de gérer plusieurs sessions de communication. Le fait de placer une session sur un blocage forcé libère la ligne/l’adresse de l’utilisateur pour effectuer d’autres appels. En règle générale, un appel en attente ne peut pas être transféré ou inclus dans un appel de conférence, mais un appel de consultation peut. Les appels de consultation sont initiés à l’aide d’opérations de [Conférence](conference-ovr.md) ou de [transfert](transfer-ovr.md) .

Une fois qu’un appel a été correctement mis en attente, l’état de l’appel passe généralement à l’État onHold. Lorsqu’un appel est en attente, l’application peut recevoir des messages sur les modifications d’état de l’appel en attente. Par exemple, si le tiers détenu raccroche, l’état de l’appel peut passer à déconnecté.

Dans une situation de pont, l’opération de maintien peut ne pas réellement placer l’appel en attente. L’état des autres stations de l’appel peut régir (par exemple, la tentative de « conservation » d’un appel lorsque d’autres stations participantes n’est pas possible); au lieu de cela, l’appel peut simplement être remplacé par l’état inactif alors qu’il reste connecté sur d’autres stations.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3. x :** Consultez [**ITBasicCallControl :: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
