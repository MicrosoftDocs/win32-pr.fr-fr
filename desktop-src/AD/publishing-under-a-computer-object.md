---
title: Publication sous un objet ordinateur
description: En règle générale, les services basés sur l’hôte créent des SCP sous l’objet ordinateur pour l’ordinateur hôte. Les services basés sur l’hôte sont des services étroitement liés à un seul ordinateur hôte.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842038"
---
# <a name="publishing-under-a-computer-object"></a>Publication sous un objet ordinateur

En règle générale, les services basés sur l’hôte créent des SCP sous l’objet ordinateur pour l’ordinateur hôte. Les services basés sur l’hôte sont des services étroitement liés à un seul ordinateur hôte.

**Pour créer des SCP sous un objet ordinateur**

1.  Appelez la fonction [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) pour obtenir le nom unique (DN) dans le répertoire de l’objet ordinateur de l’ordinateur local.
2.  Utilisez ce DN pour établir une liaison à l’objet ordinateur et créer le SCP.

Pour plus d’informations et pour obtenir un exemple de code, consultez [Comment les clients recherchent et utilisent un point de connexion de service](how-clients-find-and-use-a-service-connection-point.md).

N’oubliez pas que seuls les ordinateurs membres du domaine disposent d’objets ordinateur valides dans le répertoire.

Pour récupérer le nom DNS ou NetBIOS de l’ordinateur local, appelez la fonction [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

 

 