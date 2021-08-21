---
title: Implémentation du décompte de références
description: Implémentation du décompte de références
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa2a3e9827d35d07fa88b62c6f1097fcb3ad3ae3b5b75764deeac1c9c271050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048157"
---
# <a name="implementing-reference-counting"></a>Implémentation du décompte de références

Le décompte de références requiert un travail sur la partie de l’implémenteur d’une classe et des clients qui utilisent des objets de cette classe. Lorsque vous implémentez une classe, vous devez implémenter les méthodes [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dans le cadre de l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Ces deux méthodes ont les implémentations simples suivantes :

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrémente le décompte de références internes de l’objet.
-   [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) First décrémente le décompte de références internes de l’objet, puis vérifie si le nombre de références est tombé à zéro. Si c’est le cas, cela signifie que personne n’utilise plus l’objet, donc la fonction **Release** libère l’objet.

Une approche d’implémentation courante pour la plupart des objets consiste à avoir une seule implémentation de ces méthodes (avec [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), qui est partagée entre toutes les interfaces et, par conséquent, un nombre de références qui s’applique à l’ensemble de l’objet. Toutefois, du point de vue du client, le décompte de références est strictement et clairement une notion par pointeur d’interface. par conséquent, les objets qui tirent parti de cette fonctionnalité en construisant, détruisant, chargent ou déchargent de façon dynamique des parties de leur fonctionnalité en fonction des pointeurs d’interface actuellement existants peuvent être implémentés. Il s’agit d' *interfaces de destruction*.

Chaque fois qu’un client appelle une méthode (ou une fonction API), telle que [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), qui retourne un nouveau pointeur d’interface, la méthode appelée est chargée d’incrémenter le décompte de références via le pointeur retourné. Par exemple, lorsqu’un client crée d’abord un objet, il reçoit un pointeur d’interface vers un objet qui, du point de vue du client, a un décompte de références d’un. Si le client appelle ensuite [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur le pointeur d’interface, le nombre de références devient deux. Le client doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) deux fois sur le pointeur d’interface pour supprimer toutes ses références à l’objet.

Un exemple de la façon dont les décomptes de références sont strictement par pointeur d’interface se produit lorsqu’un client appelle [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le premier pointeur pour une nouvelle interface ou la même interface. Dans l’un ou l’autre de ces cas, le client doit appeler une fois la [**mise en sortie**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour chaque pointeur. COM ne requiert pas qu’un objet retourne le même pointeur lorsqu’il demande plusieurs fois la même interface. (La seule exception est une requête vers [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), qui identifie un objet à com.) Cela permet à l’implémentation d’objet de gérer efficacement les ressources.

La sécurité des threads est également un problème important dans l’implémentation de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Pour plus d’informations, consultez [processus, threads et Apartments](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des durées de vie des objets via le décompte de références](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 