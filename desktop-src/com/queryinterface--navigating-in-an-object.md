---
title: QueryInterface, navigation dans un objet
description: QueryInterface, navigation dans un objet
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbb25f76f87b43f6fc4fc4d3a1a3eb65c19960942769818a83f176fc62f72c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611069"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface : navigation dans un objet

Une fois que vous avez un pointeur initial vers une interface sur un objet, COM a un mécanisme très simple pour déterminer si l’objet prend en charge une autre interface spécifique et, si tel est le cas, pour obtenir un pointeur vers celui-ci. (Pour plus d’informations sur l’obtention d’un pointeur initial vers une interface sur un objet, consultez [obtention d’un pointeur vers un objet](getting-a-pointer-to-an-object.md).) Ce mécanisme est la méthode [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) de l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Si l’objet prend en charge l’interface demandée, la méthode doit retourner un pointeur vers cette interface. Cela permet à un objet de naviguer librement parmi les interfaces prises en charge par un objet. **QueryInterface** sépare la demande « prenez-vous en charge un contrat donné ? » de l’utilisation hautes performances de ce contrat une fois les négociations réussies.

Lorsqu’un client accède initialement à un objet, ce client reçoit au minimum un pointeur d’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (l’interface la plus fondamentale) par le biais duquel il peut contrôler la durée de vie de l’objet, en disant à l’objet quand il a terminé d’utiliser l’objet, et appeler [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). Le client est programmé pour demander à chaque objet qu’il gère d’effectuer certaines opérations, mais l’interface **IUnknown** n’a aucune fonction pour ces opérations. Au lieu de cela, ces opérations sont exprimées par d’autres interfaces. Le client est donc programmé pour négocier avec des objets pour ces interfaces. Plus précisément, le client appellera **QueryInterface** pour demander à un objet une interface par le biais de laquelle le client peut appeler les opérations souhaitées.

Étant donné que l’objet implémente [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), il a la possibilité d’accepter ou de rejeter la demande. Si l’objet accepte la demande du client, **QueryInterface** retourne un nouveau pointeur vers l’interface demandée au client. Par le biais de ce pointeur d’interface, le client a accès aux méthodes de cette interface. Si, en revanche, l’objet rejette la demande du client, **QueryInterface** retourne un pointeur null (une erreur) et le client n’a aucun pointeur via lequel appeler les fonctions souhaitées. Dans ce cas, le client doit s’adapter correctement à cette éventualité. Par exemple, supposons qu’un client ait un pointeur vers l’interface A sur un objet et demande les interfaces B et C. Supposons également que l’objet prenne en charge l’interface B, mais ne prend pas en charge l’interface C. Le résultat est que l’objet retourne un pointeur vers B et signale que C n’est pas pris en charge.

Un point important est que lorsqu’un objet rejette un appel à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), il est impossible pour le client de demander à l’objet d’effectuer les opérations exprimées par le biais de l’interface demandée. Un client doit avoir un pointeur d’interface pour appeler des méthodes dans cette interface. Si l’objet refuse de fournir le pointeur demandé, le client doit être prêt à le faire sans, soit en n’utilisant pas tout ce qu’il avait prévu d’effectuer avec cet objet, soit en tentant de revenir sur un autre interface, peut-être moins puissante. Cette fonctionnalité de la fonctionnalité COM fonctionne bien en comparaison avec d’autres systèmes orientés objet dans lesquels vous ne pouvez pas savoir si une fonction fonctionnera tant que vous n’aurez pas appelé cette fonction, et même si la gestion de l’échec est incertaine. **QueryInterface** offre un moyen fiable et cohérent de savoir si un objet prend en charge une interface avant de tenter d’appeler ses méthodes.

La méthode [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) offre également un moyen fiable et fiable pour un objet d’indiquer qu’il ne prend pas en charge un contrat donné. Autrement dit, si dans un appel à **QueryInterface** , il demande un objet « Old », qu’il prenne en charge une interface « New » (par exemple, qui a été inventée après l’envoi de l’ancien objet), l’ancien objet sera fiable, sans provoquer de blocage, répondez « non ». La technologie qui prend en charge cette technologie est l’algorithme par lequel les IID sont alloués. Bien que cela puisse paraître un petit point, il est extrêmement important de l’architecture globale du système, et la possibilité de rechercher des éléments hérités concernant les nouvelles fonctionnalités est, étonnamment, une fonctionnalité qui n’est pas présente dans la plupart des autres architectures d’objets.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation et implémentation de IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




