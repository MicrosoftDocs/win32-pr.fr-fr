---
title: Conteneurs de contenu
description: Conteneurs de contenu
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Magasins en ligne du lecteur Windows Media, conteneurs de contenu
- magasins en ligne, conteneurs de contenu
- types 1 magasins en ligne, conteneurs de contenu
- Windows Media Player Online stores, interface IWMPContentContainer
- magasins en ligne, interface IWMPContentContainer
- types 1 magasins en ligne, interface IWMPContentContainer
- Windows Media Player, conteneurs de contenu
- Lecteur Windows Media, interface IWMPContentContainer
- conteneurs de contenu
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "106542845"
---
# <a name="content-containers"></a>Conteneurs de contenu

Le lecteur Windows Media utilise des conteneurs de contenu pour représenter le contenu multimédia numérique dans un téléchargement d’abonnement ou une transaction d’achat. Un conteneur de contenu est représenté par l’interface **IWMPContentContainer** . Un conteneur de contenu peut contenir une liste de contenu associé, tel qu’un album, ou un ensemble d’éléments de contenu non liés, ou des *suivis*. Vous pouvez utiliser l’interface **IWMPContentContainer** pour énumérer les pistes du conteneur de contenu et récupérer le prix de chaque piste. Vous pouvez également récupérer des informations sur le conteneur de contenu lui-même, telles que l’ID de conteneur, le type de contenu dans le conteneur et le prix total des pistes dans le conteneur (qui peut être différent de la somme des prix des différentes pistes, comme dans le cas d’un achat d’album).

Pour fournir un mécanisme d’empaquetage de plusieurs conteneurs de contenu dans un seul objet, le lecteur Windows Media prend en charge l’interface **IWMPContentContainerList** . **IWMPContentContainerList** fournit des méthodes pour énumérer et récupérer les conteneurs de contenu de la liste. Pour déterminer si la liste de conteneurs de contenu représente un achat ou un téléchargement d’abonnement, appelez [IWMPContentContainerList :: GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) pour récupérer une valeur [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentContainer**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**Interface IWMPContentContainerList**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




