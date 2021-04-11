---
title: Création et gestion d’un point de connexion de service
description: Lors de la publication avec un SCP, n’oubliez pas qu’il doit contenir les données actuelles sur l’instance de service.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Création et gestion d’une publicité de point de connexion de service
- point de connexion de service Active Directory, création et maintenance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031029"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a>Création et gestion d’un point de connexion de service

Lors de la publication avec un SCP, n’oubliez pas qu’il doit contenir les données actuelles sur l’instance de service. Dans le cas contraire, les clients qui se lient au SCP récupèrent les données obsolètes. Votre programme d’installation de service, qui crée un SCP, spécifie les valeurs initiales des attributs SCP. Ensuite, lorsque l’instance de service démarre, elle doit localiser le SCP et mettre à jour les valeurs d’attribut, si nécessaire. De cette façon, les clients sont assurés des données les plus récentes.

Après avoir créé le SCP, votre programme d’installation de service effectue deux étapes supplémentaires qui permettent à votre service de mettre à jour le SCP :

-   Définissez les ACE dans le descripteur de sécurité de l’objet SCP pour permettre au service de modifier les attributs SCP au moment de l’exécution. Pour plus d’informations et pour obtenir un exemple de code, consultez [activation du compte de service pour accéder aux propriétés SCP](enabling-service-account-to-access-scp-properties.md).
-   Mettez en cache l' **objectGUID** du SCP dans le registre sur l’ordinateur hôte du service. Le service récupère le GUID mis en cache à lier au SCP pour vérifier et mettre à jour ses attributs.

Le programme d’installation du service met en cache l' **objectGUID** du SCP plutôt que son DN. L' **objectGUID** n’est jamais modifié, que le SCP soit déplacé ou renommé. Le DN peut changer si un administrateur déplace ou renomme le SCP. Par exemple, si vous créez un SCP en tant qu’enfant d’un objet ordinateur, le nom unique du SCP change si l’ordinateur est renommé ou déplacé vers un autre domaine ou une autre unité d’organisation.

Lorsqu’un programme d’installation de service crée un SCP, il doit lire l' **objectGUID** de l’objet nouvellement créé et le mettre en cache dans le registre de l’ordinateur hôte du service. Utilisez la méthode de [**\_ GUID IADs :: obtenir**](/windows/desktop/ADSI/iads-property-methods) pour obtenir la valeur **objectGUID** dans un format de chaîne adapté à la liaison. Mettez en cache la chaîne GUID sous la forme d’une valeur sous la clé de Registre suivante.

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

Où « nom du fournisseur » et « nom du produit » identifient le fournisseur et le produit.

Lorsque le service démarre, il récupère la chaîne GUID mise en cache à partir du Registre et l’utilise pour établir une liaison avec le SCP. Le service lit les attributs SCP importants et les compare aux valeurs actuelles. Si les valeurs SCP sont obsolètes, le service les met à jour. Les valeurs que le service peut nécessiter pour mettre à jour incluent les **Mots clés**, **serviceBindingInformation**, **servicednsname** et **serviceDNSNameType**.

## <a name="examples"></a>Exemples

-   [Exemples de scripts](script-samples-for-managing-service-connection-points.md)
-   [Exemples de code (C/C++)](code-samples-for-managing-service-connection-points.md)

 

 