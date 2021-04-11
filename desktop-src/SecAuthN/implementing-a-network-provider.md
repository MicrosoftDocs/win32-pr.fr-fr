---
description: Un fournisseur réseau est une DLL qui permet au système d’exploitation Windows de prendre en charge un protocole réseau spécifique.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implémentation d’un fournisseur de réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112191"
---
# <a name="implementing-a-network-provider"></a>Implémentation d’un fournisseur de réseau

Un fournisseur réseau est une DLL qui permet au système d’exploitation Windows de prendre en charge un protocole réseau spécifique. Pour ce faire, il implémente l’API du fournisseur réseau. Cette API est un ensemble de fonctions que le [*routeur multifournisseur*](../secgloss/m-gly.md) (MPR) appelle pour communiquer avec le réseau. Le fournisseur réseau convertit ensuite ces appels en appels d’API spécifiques au réseau pour effectuer l’action spécifiée par le MPR. De cette façon, le système d’exploitation Windows peut interagir avec les nouveaux protocoles réseau sans avoir à comprendre leurs API spécifiques au réseau.

Pour créer un fournisseur réseau, écrivez une DLL qui exporte la fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) .

La prise en charge des autres fonctions dans l’API du fournisseur réseau est facultative. Si votre fournisseur de réseau n’a pas besoin d’une fonction, votre DLL n’a pas besoin de l’implémenter ou de fournir une implémentation de stub. Pour plus d’informations, consultez les rubriques relatives aux [fonctions](authentication-functions.md)individuelles dans fonctions du fournisseur de réseau.

L’exception est que si vous prenez en charge l’une des fonctions d’énumération suivantes, vous devez prendre en charge les deux autres fonctions également : [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)et [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

Les instructions suivantes décrivent comment écrire un fournisseur réseau qui interagit correctement avec le système d’exploitation MPR et Windows. Dans la mesure du possible, votre fournisseur doit respecter les instructions suivantes pour la vitesse, la validation et le routage.

## <a name="speed"></a>Vitesse

Un fournisseur de réseau doit déterminer rapidement si une ressource réseau est la sienne. Cela est dû au fait que le MPR peut devoir parcourir de nombreux fournisseurs pour trouver le propriétaire d’une ressource.

Si le fournisseur réseau ne possède pas la ressource, il doit immédiatement retourner le \_ code d' \_ État du NetName WN.

Il est également important que les fournisseurs qui prennent en charge [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) retournent des résultats pour cette fonction rapidement parce qu’ils sont appelés alors que winfile dessine l’arborescence de répertoires.

## <a name="validation"></a>Validation

L’ordre de validation est important. Un fournisseur réseau doit d’abord déterminer si son réseau est démarré, puis déterminer si le réseau et le fournisseur de réseau prennent en charge l’opération. Si, après ces vérifications, le fournisseur réseau reçoit des ressources réseau, il doit déterminer s’il les possède. Enfin, il doit valider d’autres paramètres.

## <a name="routing"></a>Routage

Si le MPR doit parcourir les fournisseurs de réseau, il essaiera tous les fournisseurs jusqu’à ce que l’un d’eux accepte l’appel. En d’autres termes, le MPR continue toujours à essayer de trouver un fournisseur de réseau.

Toutefois, elle prend note de la première erreur importante signalée par un fournisseur. Des erreurs telles qu’une erreur de type \_ \_ netpath, une erreur de nom de \_ réseau incorrect, une erreur de \_ \_ \_ paramètre non valide \_ , \_ le niveau d’erreur non valide \_ sont considérés comme non significatifs, car ils signifient simplement que le fournisseur ne gère pas la ressource. Toutefois, si le fournisseur échoue avec l’erreur erreur \_ \_ mot de passe non valide ou une autre erreur significative, MPR enregistre cette erreur et continue de parcourir les fournisseurs réseau. En général, lors du routage, si aucun fournisseur n’accepte l’appel, le MPR signale la première erreur significative qu’il rencontre lors du cycle via les fournisseurs réseau.

Pour déterminer le message d’erreur à renvoyer, votre fournisseur de réseau doit prendre en compte ce comportement de MPR.

## <a name="implementation-note"></a>Note d’implémentation

Lors de l’implémentation de la DLL du fournisseur réseau, le fournisseur ne doit pas appeler d’autres [fonctions de mise en réseau Windows](../wnet/windows-networking-functions.md), [API d’interpréteur](../shell/samples-usingthumbnailproviders.md)de commandes ou autres requêtes basées sur un chemin d’accès UNC qui pourraient entraîner une réentrée dans le sous-système MPR. Si vous effectuez des appels à partir d’une DLL de fournisseur réseau, l’application ou d’autres composants du système d’exploitation peuvent subir des conflits, des performances médiocres ou des blocages à l’intérieur du sous-système MPR.

 

 
