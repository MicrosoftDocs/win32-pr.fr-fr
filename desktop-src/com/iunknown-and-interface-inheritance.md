---
title: IUnknown et héritage d’interface
description: IUnknown et héritage d’interface
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521857"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown et héritage d’interface

L’héritage dans COM ne signifie pas la réutilisation du code. Étant donné qu’aucune implémentation n’est associée à des interfaces, l’héritage d’interface ne signifie pas l’héritage du code. Cela signifie uniquement que le contrat associé à une interface est hérité dans une méthode de classe de base C++ pure-virtual et modifié, soit en ajoutant de nouvelles méthodes, soit en qualifiant davantage l’utilisation autorisée des méthodes. Il n’y a pas d’héritage sélectif dans COM. Si une interface hérite d’une autre, elle comprend toutes les méthodes définies par l’autre interface.

L’héritage est utilisé avec modération dans les interfaces COM prédéfinies. Toutes les interfaces prédéfinies (et toutes les interfaces personnalisées que vous définissez) héritent de leurs définitions de l’interface importante [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), qui contient trois méthodes vitales : [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Tous les objets COM doivent implémenter l’interface **IUnknown** , car il fournit les moyens, à l’aide de **QueryInterface**, de se déplacer librement entre les différentes interfaces qu’un objet prend en charge, ainsi que les moyens de gérer sa durée de vie à l’aide de **AddRef** et **Release**.

Lors de la création d’un objet qui prend en charge l' [agrégation](aggregation.md), vous devez implémenter un ensemble de fonctions [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pour toutes les interfaces, ainsi qu’une interface **IUnknown** autonome. Dans tous les cas, tout implémenteur d’objet implémente les méthodes **IUnknown** . Pour plus d’informations, consultez la section [utilisation et implémentation de IUnknown](using-and-implementing-iunknown.md) .

Bien qu’il existe quelques interfaces qui héritent de leurs définitions d’une deuxième interface en plus de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), la majorité hérite simplement des méthodes d’interface **IUnknown** . Cela rend la plupart des interfaces relativement compactes et faciles à encapsuler.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets et interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 