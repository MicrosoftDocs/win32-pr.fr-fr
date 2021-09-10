---
title: Sécurité d’activation
description: Sécurité d’activation
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363603"
---
# <a name="activation-security"></a>Sécurité d’activation

La sécurité d’activation (également appelée « lancement de la sécurité ») permet de contrôler qui peut lancer un serveur. La sécurité d’activation est automatiquement appliquée par le gestionnaire de contrôle des services (SCM) d’un ordinateur particulier. À la réception d’une demande d’activation d’un objet par un client (comme décrit dans [fonctions d’assistance de création d’instance](instance-creation-helper-functions.md)), le SCM vérifie la demande par rapport aux informations de sécurité d’activation stockées dans son registre. (La sécurité d’activation est également vérifiée pour les activations du même ordinateur.)

Lors de la détermination de l’identité du client, l’activation examine l’indicateur de masquage défini dans l’appel du client à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si l’indicateur de masquage est défini (pour le masquage dynamique ou statique), le jeton de thread est utilisé, le cas échéant, pour déterminer l’identité du client. Si aucun voilage n’est défini, le jeton de processus est utilisé à la place du jeton de thread.

Pour plus d’informations sur la sécurité de l’activation, consultez [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) et [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 