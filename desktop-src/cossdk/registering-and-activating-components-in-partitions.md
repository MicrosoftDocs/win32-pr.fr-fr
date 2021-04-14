---
description: Inscription et activation de composants dans des partitions
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Inscription et activation de composants dans des partitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523532"
---
# <a name="registering-and-activating-components-in-partitions"></a>Inscription et activation de composants dans des partitions

Une fois qu’une partition a été créée, l’étape suivante consiste à inscrire vos composants COM+ au sein de cette partition. Un composant est inscrit dans une partition lors de la création d’une nouvelle application COM+ ou lors de l’installation d’une application COM+ existante dans la partition. Pour faciliter l’administration de l’inscription lorsque plusieurs partitions contiennent les mêmes composants COM+, le service partitions permet à un administrateur de copier des applications ou des composants d’une partition vers une autre. Lorsqu’une application COM+ ou un composant est copié, toutes les propriétés de partition associées sont copiées avec celle-ci, à l’exception de l’identité de l’application ou de l’un des membres d’un rôle.

Lorsque le programme client appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) pour instancier un objet, com+ effectue deux étapes distinctes, comme suit :

1.  Localise la partition dans laquelle le composant réside
2.  Localise le composant approprié dans cette partition

Les rubriques suivantes de cette section décrivent ces étapes en détail :

-   [Recherche de partitions pendant l’activation](locating-partitions-during-activation.md)
-   [Recherche d’un composant pour l’activation](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions relatives à la conception d’applications](application-design-restrictions.md)
</dt> <dt>

[Composants et partitions COM+ en file d’attente](com--queued-components-and-partitions.md)
</dt> <dt>

[Implémentation de la partition](partition-implementation.md)
</dt> <dt>

[Que sont les partitions COM+ ?](what-are-com--partitions-.md)
</dt> </dl>

 

 
