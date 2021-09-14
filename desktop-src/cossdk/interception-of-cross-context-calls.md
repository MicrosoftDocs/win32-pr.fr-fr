---
description: Lorsqu’un objet est activé dans un contexte donné, les appels suivants à ou à partir de celui-ci, dans le contexte, sont gérés différemment des appels à travers la limite de contexte.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interception d’appels entre les contextes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118489"
---
# <a name="interception-of-cross-context-calls"></a>Interception d’appels entre les contextes

Lorsqu’un objet est activé dans un contexte donné, les appels suivants à ou à partir de celui-ci, dans le contexte, sont gérés différemment des appels à travers la limite de contexte. Les appels à travers la limite de contexte sont gérés avec les proxies légers. Ces proxies gèrent la médiation requise pour ajuster l’environnement d’exécution à partir d’un autre qui adapte l’appelant à un qui prend en charge l’appelé. Ce processus est appelé *interception*.

L’interception des appels entre les contextes est nécessaire, car les objets dans des contextes différents ont des exigences d’exécution différentes, ce qui est précisément la raison des contextes. COM+ intercepte les références d’objet que vous passez en tant que paramètres de méthode et les convertit automatiquement en proxies afin qu’ils soient utilisables dans le nouveau contexte.

Si vous partagez des références d’objet entre des limites de contexte par d’autres moyens (par exemple, dans des variables globales), vous devez toujours utiliser [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) et [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). Ces fonctions peuvent traduire une référence d’objet en un proxy utilisable dans un contexte différent. Ne partagez jamais une référence d’objet brut entre les limites de contexte.

Le comportement des appels à travers le contexte peut avoir des conséquences indésirables dans le cas d’objets exposant des interfaces qui ne peuvent pas être marshalées. Dans ce cas, vous souhaiterez probablement insister sur le fait que l’objet qui ne peut pas être marshalé soit uniquement activé dans le contexte de son appelant et jamais dans son propre contexte. Pour ce faire, sélectionnez l’option **doit être activé dans le contexte** de l’appelant sous l’onglet **activation** de la page **Propriétés** du composant. (Pour obtenir des instructions pas à pas, consultez [application de l’activation dans le contexte de l’appelant](enforcing-activation-in-the-caller-s-context.md) .)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation du contexte](context-activation.md)
</dt> </dl>

 

 
