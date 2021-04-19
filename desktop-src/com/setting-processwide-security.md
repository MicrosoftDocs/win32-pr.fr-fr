---
title: Définition de la sécurité Process-Wide
description: Il existe plusieurs façons de définir la sécurité au niveau du processus.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511456"
---
# <a name="setting-process-wide-security"></a>Définition de la sécurité Process-Wide

Il existe plusieurs façons de définir la sécurité au niveau du processus. La première méthode, à l’aide de l’outil Dcomcnfg.exe, est plus simple, car elle ne nécessite pas de programmation. La deuxième technique offre au programmeur davantage de contrôle et nécessite un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Une autre technique consiste à définir la sécurité au niveau du processus dans le registre à l’aide de la clé [AppID](appid-key.md) .

Pour plus d’informations sur ces techniques, consultez les rubriques suivantes :

-   [Définition de la sécurité Process-Wide à l’aide de DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Définition de la sécurité Process-Wide avec CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Définition de la sécurité Process-Wide dans le registre](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité au niveau du proxy d’interface](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




