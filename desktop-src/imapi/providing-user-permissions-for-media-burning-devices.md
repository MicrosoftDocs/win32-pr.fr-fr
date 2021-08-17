---
title: Fournir des autorisations utilisateur pour les appareils de gravure de médias
description: par défaut, Windows Vista et Windows Server 2008 accordent un accès en lecture/écriture aux administrateurs et aux utilisateurs connectés directement à l’ordinateur (utilisateurs intermédiaires).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c5827b960405855ba34880e39750b39d4f934e395167479b7cae7912721af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758559"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Fournir des autorisations utilisateur pour les appareils de gravure de médias

par défaut, Windows Vista et Windows Server 2008 accordent un accès en lecture/écriture aux administrateurs et aux utilisateurs connectés directement à l’ordinateur (utilisateurs intermédiaires). toutefois, dans Windows XP et Windows Server 2003, un administrateur doit accorder ces privilèges de lecture/écriture à d’autres groupes d’utilisateurs.

Un administrateur peut ajuster des autorisations spécifiques à un appareil pour les utilisateurs avec pouvoir et les utilisateurs interactifs.

pour accéder au panneau autorisations du groupe approprié dans Windows XP, cliquez sur **démarrer**, sur **exécuter**, tapez **gpedit. msc**, puis cliquez sur **OK**. dans l’interface stratégie de groupe, développez successivement **Configuration ordinateur**, **Windows Paramètres**, **Paramètres de sécurité**, **stratégies locales**, puis double-cliquez sur **Options de sécurité**.

![Capture d’écran montrant la fenêtre « stratégie de groupe » avec une stratégie sélectionnée à partir du volet « stratégie ».](images/gpolpanel.jpg)

Dans ce panneau, un administrateur doit spécifier les paramètres de deux options d’appareil pour fournir les autorisations de groupe requises :

-   Définir « appareils : restreindre l’accès à un CD-ROM à un utilisateur connecté localement » à **activé**
-   Définissez « appareils : autorisés à formater et éjecter les supports amovibles » pour **les administrateurs et les utilisateurs avec pouvoir**. il est également possible d’émuler Windows autorisations Vista en affectant à cette option la valeur **administrateurs et utilisateurs interactifs**.

bien qu’une interface utilisateur spécifique n’existe pas dans Windows XP ou Windows Server 2003 pour l’utilisation de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) ou [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), il est possible d’utiliser ces api pour accorder des autorisations d’appareil aux groupes d’utilisateurs personnalisés. Par exemple, un appel à **SetSecurityInfo** accorde des autorisations à des groupes d’utilisateurs. Les modifications apportées aux autorisations avec cette API sont temporaires et ne sont pas conservées au redémarrage. Toutefois, l’appel de [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implémente les modifications d’autorisation dans le registre, qui sont conservées au cours d’un redémarrage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’IMAPi](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 