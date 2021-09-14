---
title: Clients moniker
description: Les clients moniker doivent commencer par obtenir un moniker, et il existe plusieurs façons pour un client moniker d’obtenir un moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855441"
---
# <a name="moniker-clients"></a>Clients moniker

Les clients moniker doivent commencer par obtenir un moniker, et il existe plusieurs façons pour un client moniker d’obtenir un moniker. Par exemple, dans les documents composés OLE, lorsque l’utilisateur final crée un élément lié (à l’aide de la boîte de dialogue **Insérer un objet** , du presse-papiers ou du glisser-déplacer), un moniker est incorporé dans le cadre de l’élément lié. Dans ce cas, le programmeur a un contact minimal avec les monikers. Par programmation, si vous avez un pointeur d’interface vers un objet qui implémente l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , vous pouvez l’utiliser pour obtenir un moniker, et il existe des méthodes sur d’autres interfaces définies pour retourner des monikers.

Il existe différents types de monikers, qui sont utilisés pour identifier différents genres d’objets, mais pour un client moniker, tous les monikers ont le même aspect. Un client moniker appelle simplement [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur un moniker et obtient un pointeur d’interface vers l’objet que le moniker identifie. Que le moniker identifie un objet aussi grand qu’une feuille de calcul entière ou aussi petit qu’une cellule unique dans une feuille de calcul, l’appel de **BindToObject** retourne un pointeur vers cet objet. Si l’objet est déjà en cours d’exécution, **BindToObject** le trouvera en mémoire. Si l’objet est stocké passivement sur le disque, **BindToObject** localise un serveur pour cet objet, exécute le serveur et fait en sorte que le serveur remet l’objet à l’État en cours d’exécution. Tous les détails du processus de liaison sont masqués dans le client moniker. Ainsi, pour un client moniker, l’utilisation du moniker est très simple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs de moniker](moniker-providers.md)
</dt> <dt>

[Implémentations du moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




