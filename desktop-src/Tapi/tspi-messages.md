---
description: Cette section contient la liste des messages dans l’interface TSPI (Telephony Service Provider Interface).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: Messages TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5772a1ccb0c07f03b2a17348ecf5e4834bb97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535567"
---
# <a name="tspi-messages"></a>Messages TSPI

Cette section contient la liste des messages dans l’interface TSPI (Telephony Service Provider Interface). Ces messages sont utilisés pour notifier l’interface TAPI de l’occurrence d’événements asynchrones qui se produisent spontanément au sein du fournisseur de services. Le fournisseur de services transmet ces événements à l’interface TAPI en appelant une fonction de rappel [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) ou [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) , selon que le fournisseur de services signale ou non un événement sur une ligne, un appel ou un appareil téléphonique. La procédure **LINEEVENT** pour signaler des événements qui se produisent sur une ligne ou un appel est fournie au fournisseur de services au moment où la ligne est ouverte à l’aide de la fonction [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) . La procédure **PHONEEVENT** pour signaler les événements qui se produisent sur un téléphone est fournie avec la fonction [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) .

Ces événements spontanés ne sont pas sollicités par l’interface TAPI dans le sens où ils ne constituent pas une réponse directe à une demande. Ces événements diffèrent de ceux qui signalent la fin des requêtes effectuées par l’interface TAPI. Ces événements d’achèvement sont signalés par le biais de la fonction de rappel d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Les profils de paramètre des procédures événementielles spontanées incluent des paramètres qui identifient l’objet approprié pour lequel l’événement est signalé (téléphone, ligne ou appel). L’identification se présente sous la forme d’un handle opaque dont l’interprétation exacte n’est pas publiée par TSPI. L’interface TAPI détermine en interne la relation entre ces handles opaques et les structures de données utilisées pour représenter les appareils.

Le profil de paramètre des procédures événementielles spontanées comprend également un paramètre de message identifiant le type du message. Chaque type de message a une définition correspondante qui détermine les descripteurs inclus, ainsi que d’autres paramètres et leurs significations. Il existe une forte correspondance entre les messages qui s’affichent au niveau du TSPI et ceux qui apparaissent au niveau de l’interface TAPI. Il s’agit des règles générales de correspondance :

-   L’ensemble de messages est quasiment identique. Lorsque les messages correspondent, le même nom et la même valeur de message sont utilisés au niveau TSPI.
-   Les handles qui s’affichent au niveau TSPI sont les types opaques définis par la spécification TSPI. Ces types (et leur interprétation) diffèrent de ceux au niveau de l’interface TAPI, bien qu’ils fassent référence à la même classe de périphérique. Par exemple, lorsqu’un message TAPI inclut un handle HLINE, le message TSPI correspondant inclut généralement un handle [**HTAPILINE**](htapiline.md) .
-   Aucune donnée *dwCallbackInstance* n’est passée au rappel.
-   Les paramètres *dwParam1*, *dwParam2* et *dwParam3* sont généralement identiques aux paramètres correspondants pour le message TAPI.
-   Les messages orientés ligne et orientés appel sont passés à une procédure de rappel différente des messages orientés vers le téléphone.

Pour chaque message, cette section répertorie les éléments suivants :

-   L’objectif du message
-   Procédure de rappel à laquelle ce message est passé
-   Description des paramètres du message
-   Commentaires facultatifs sur l’utilisation du message
-   Références facultatives à d’autres fonctions, messages et structures de données
-   Commentaires facultatifs comparant ce message à l’interface TAPI

Certains messages sont utilisés pour notifier à l’interface TAPI une modification de l’état d’un objet. Ces messages fournissent le descripteur d’objet opaque opaque et une indication de l’élément d’état modifié. TAPI peut ensuite appeler une fonction « obtenir l’État » appropriée de l’objet pour obtenir l’état complet de l’objet.

Lorsqu’un événement se produit, un message peut ou non être envoyé à l’interface TAPI. Pour certains types d’événements, tels que les changements d’État, TAPI spécifie un ensemble de modifications d’État qui l’intéressent. Le fournisseur de services est invité à limiter les événements de message de modification d’État qu’il signale à ceux inclus dans cet ensemble. Le fournisseur de services n’est pas tenu de respecter cette limite. En d’autres termes, il peut signaler plus de modifications que ce qui est strictement nécessaire. Toutefois, il doit essayer d’observer la limite pour des raisons de performances.

Le message de réponse de ligne \_ n’est pas utilisé au niveau TSPI. La fin d’une requête asynchrone est signalée à l’aide du rappel d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Le \_ message de réponse téléphonique n’est pas utilisé au niveau TSPI. La fin d’une requête asynchrone est signalée à l’aide du rappel d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Pour plus d'informations, consultez les rubriques suivantes :

-   [Messages du périphérique de ligne TSPI](tspi-line-device-messages.md)
-   [Messages de l’appareil TSPI Phone](tspi-phone-device-messages.md)

 

 
