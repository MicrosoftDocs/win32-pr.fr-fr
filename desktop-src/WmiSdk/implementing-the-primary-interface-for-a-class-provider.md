---
description: 'Il existe deux façons d’implémenter un fournisseur de classe : implémentez l’interface en tant que fournisseur de notifications push, ou en tant que fournisseur d’extraction.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ef1b31e1228b832e4d23945f3af0c4df223ddd3edebdd1ec6e34e0e0e8d449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030439"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implémentation de l’interface principale pour un fournisseur de classes

Il existe deux façons d’implémenter un fournisseur de classe : implémentez l’interface en tant que fournisseur de notifications push, ou en tant que fournisseur d’extraction.

Les sections suivantes sont présentées dans cette rubrique :

-   [Implémentation de l’interface principale pour un fournisseur de classes Push](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implémentation de l’interface principale pour un fournisseur de classe pull](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implémentation de l’interface principale pour un fournisseur de classes Push

Tandis que tous les fournisseurs implémentent [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour l’initialisation et au moins une autre interface comme interface principale, un fournisseur Push implémente uniquement **IWbemProviderInit**.

Assurez-vous que votre implémentation effectue les tâches suivantes :

-   Récupère les données de classe appropriées.
-   Place les données dans l’espace de stockage WMI.
-   Supprime les données obsolètes.

À l’issue du processus d’initialisation, WMI gère toutes les demandes d’application pour les classes appartenant au fournisseur Push sans aucune interaction supplémentaire du fournisseur. Ensuite, le fournisseur Push agit efficacement comme un client de WMI plutôt qu’un fournisseur. Pour plus d’informations sur l’implémentation de [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), consultez [initialisation d’un fournisseur](initializing-a-provider.md).

> [!Note]  
> Lors de l’appel de WMI pour créer, mettre à jour ou supprimer des données dans un fournisseur push, définissez le paramètre *lFlags* pour inclure l’indicateur de **\_ \_ \_ mise à jour du propriétaire de l’indicateur WBEM** dans tous les appels aux méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implémentation de l’interface principale pour un fournisseur de classe pull

Un fournisseur d’extraction de classe doit implémenter [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) en tant qu’interface principale. L’interface **IWbemServices** prend en charge la récupération des données, la mise à jour des données, la suppression des données, l’énumération et le traitement des requêtes. Toutefois, étant donné que **IWbemServices** est également utilisé par les applications et les fournisseurs pour demander des services de WMI, **IWbemServices** contient de nombreuses méthodes qui ne sont pas pertinentes pour un fournisseur de classe. Votre implémentation doit prendre en charge la récupération de classe et l’énumération, par le biais des méthodes [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) et [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) , respectivement. Le tableau suivant répertorie les autres méthodes **IWbemServices** asynchrones que vous pouvez implémenter pour un fournisseur de classe.



| Méthode                                                     | Fonctionnalité      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modification |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Suppression     |



 

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

Votre fournisseur de classe doit fournir une implémentation de stub qui retourne le **\_ fournisseur WBEM E \_ \_ non \_ compatible** pour toutes les autres méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) qui ne prennent pas en charge votre jeu de fonctionnalités. Plus précisément, WMI ne prend pas en charge le traitement des requêtes pour les fournisseurs de classes. Par conséquent, un fournisseur de classe doit retourner le **\_ fournisseur WBEM E qui n’est pas en \_ \_ \_ mesure** de son implémentation de [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), définir sa propriété d’inscription **QuerySupportLevels** sur **null**, ou les deux.

Les interfaces implémentées par un fournisseur de classes sont très similaires aux interfaces d’un fournisseur d’instances et d’un fournisseur de méthode. En fait, un seul fournisseur peut agir comme les trois types de fournisseur en implémentant toutes les méthodes et en s’inscrivant correctement.

 

 



