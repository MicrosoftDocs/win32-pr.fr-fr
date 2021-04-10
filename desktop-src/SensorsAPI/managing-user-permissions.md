---
description: L’API de capteur fournit une méthode que vous pouvez utiliser pour inviter l’utilisateur à entrer des autorisations d’utilisation d’un capteur ou d’une collection de capteurs.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Gestion des autorisations utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951071"
---
# <a name="managing-user-permissions"></a>Gestion des autorisations utilisateur

L’API de capteur fournit une méthode que vous pouvez utiliser pour inviter l’utilisateur à entrer des autorisations d’utilisation d’un capteur ou d’une collection de capteurs.

Étant donné que les capteurs peuvent révéler des informations sensibles, Windows requiert que les utilisateurs activent les capteurs avant que votre programme puisse accéder aux données.

Vous souhaiterez peut-être demander une autorisation lorsque vous souhaitez utiliser des capteurs pour lesquels l’accès à l’état du capteur [**SensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) en cours est \_ \_ \_ refusé.

Pour demander des autorisations, appelez la méthode [**ISensorManager :: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) . Lorsque vous appelez cette méthode, Windows ouvre la boîte de dialogue **activer les capteurs** pour inviter l’utilisateur à activer les capteurs que vous avez demandés. Cette boîte de dialogue fournit à l’utilisateur les noms des capteurs que vous avez demandés. L’utilisateur peut choisir l’une des options suivantes :

-   **Activez ces capteurs**.
-   **N’activez pas ces capteurs**.
-   **Ouvrez le panneau de configuration pour plus d’options**.

Si un utilisateur choisit **ne pas activer ces capteurs**, Windows n’affichera pas à nouveau la boîte de dialogue **activer les capteurs** pour ces capteurs, même si votre programme appelle [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions). Si l’utilisateur choisit une autre option, Windows autorisera l’affichage de la boîte de dialogue lorsqu’elle sera demandée. Si votre appel à **RequestPermissions** contient des capteurs que l’utilisateur a précédemment choisi de conserver désactivé, l’API de capteur supprime ces capteurs de la liste des capteurs que l’utilisateur voit.

### <a name="modal-or-modeless-behavior"></a>Comportement modal ou non modal

La méthode [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) accepte un argument **booléen** qui détermine si la boîte de dialogue **activer les capteurs** est affichée en tant que fenêtre modale ou non modale. Ce paramètre affecte également si le comportement du code de retour de la boîte de dialogue est synchrone ou asynchrone.

Quand elle est modale, la boîte de dialogue a le focus exclusif sur les fenêtres d’application jusqu’à ce que l’utilisateur choisisse une option, et le code de retour **HRESULT** de votre appel à [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indique le choix de l’utilisateur. En cas de non-mode, la boîte de dialogue n’a pas le focus exclusif et votre appel à **RequestPermissions** est immédiatement retourné. Dans ce cas, le code de retour indique si la méthode a réussi, mais ne peut pas être utilisée pour déterminer le choix de l’utilisateur. Vous pouvez ensuite déterminer les capteurs qui ont été activés en gérant l’événement [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) et en vérifiant que chaque capteur a l’état de capteur \_ \_ Ready.

Pour plus d’informations sur les codes de retour, consultez la page de référence [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) .

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Meilleure pratique : Évitez les appels multiples en mode RequestPermissions

Les appels sans mode répétés à [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) affichent plusieurs instances de la boîte de dialogue **activer ces capteurs** et peuvent saturer l’écran avec des boîtes de dialogue, ce qui se traduit par une expérience utilisateur médiocre. Si vous pensez qu’après votre premier appel à **RequestPermissions**, d’autres capteurs d’emplacement pourraient être installés, nécessitant un autre appel à **RequestPermissions**, vous devez appeler **RequestPermissions** modal ou attendre que tous les capteurs d’emplacement soient installés pour effectuer un appel non modal.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Confidentialité et sécurité dans la plateforme capteur et emplacement](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Demande d’autorisations utilisateur](requesting-user-permissions.md)
</dt> </dl>

 

 
