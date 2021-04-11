---
title: Fournir des autorisations utilisateur pour les appareils de gravure de médias
description: Par défaut, Windows Vista et Windows Server 2008 accordent un accès en lecture/écriture aux administrateurs et aux utilisateurs connectés directement à l’ordinateur (utilisateurs intermédiaires).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104211167"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a>Fournir des autorisations utilisateur pour les appareils de gravure de médias

Par défaut, Windows Vista et Windows Server 2008 accordent un accès en lecture/écriture aux administrateurs et aux utilisateurs connectés directement à l’ordinateur (utilisateurs intermédiaires). Toutefois, dans Windows XP et Windows Server 2003, un administrateur doit accorder ces privilèges de lecture/écriture à d’autres groupes d’utilisateurs.

Un administrateur peut ajuster des autorisations spécifiques à un appareil pour les utilisateurs avec pouvoir et les utilisateurs interactifs.

Pour accéder au panneau autorisations appropriées du groupe dans Windows XP, cliquez sur **Démarrer**, sur **exécuter**, tapez **gpedit. msc**, puis cliquez sur **OK**. Dans l’interface stratégie de groupe, développez successivement **Configuration ordinateur**, **Paramètres Windows**, **paramètres de sécurité**, **stratégies locales**, puis double-cliquez sur **options de sécurité**.

![Capture d’écran montrant la fenêtre « stratégie de groupe » avec une stratégie sélectionnée à partir du volet « stratégie ».](images/gpolpanel.jpg)

Dans ce panneau, un administrateur doit spécifier les paramètres de deux options d’appareil pour fournir les autorisations de groupe requises :

-   Définir « appareils : restreindre l’accès à un CD-ROM à un utilisateur connecté localement » à **activé**
-   Définissez « appareils : autorisés à formater et éjecter les supports amovibles » pour **les administrateurs et les utilisateurs avec pouvoir**. Il est également possible d’émuler les autorisations Windows Vista en définissant cette option sur **administrateurs et utilisateurs interactifs**.

Bien qu’une interface utilisateur spécifique n’existe pas dans Windows XP ou Windows Server 2003 pour l’utilisation de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) ou [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), il est possible d’utiliser ces API pour accorder des autorisations d’appareil aux groupes d’utilisateurs personnalisés. Par exemple, un appel à **SetSecurityInfo** accorde des autorisations à des groupes d’utilisateurs. Les modifications apportées aux autorisations avec cette API sont temporaires et ne sont pas conservées au redémarrage. Toutefois, l’appel de [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) implémente les modifications d’autorisation dans le registre, qui sont conservées au cours d’un redémarrage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’IMAPi](using-imapi.md)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 