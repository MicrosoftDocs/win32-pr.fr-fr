---
description: Certains mouvements d’application peuvent entrer en conflit avec des caractères d’Extrême-Orient ou des combinaisons de caractères d’Extrême-Orient.
ms.assetid: 56ff773f-ef95-47f8-ba04-2593330867ee
title: Conflits avec des caractères de East-Asian
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171e6401e01bb20bede7f9291d492692c2c11f3bf61ced36a40c300f909e25f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110989"
---
# <a name="conflicts-with-east-asian-characters"></a>Conflits avec des caractères de East-Asian

Certains *mouvements d’application* peuvent entrer en conflit avec des caractères d’Extrême-Orient ou des combinaisons de caractères d’Extrême-Orient. Le tableau suivant répertorie les conflits possibles entre les gestes d’application et les caractères des applications qui ont une entrée de caractères d’Extrême-Orient spécifique.



| Mouvement                 | Chinois (simplifié) | Chinois (traditionnel) | Japonais     | Coréen       |
|-------------------------|----------------------|-----------------------|--------------|--------------|
| Descendre<br/>         | X<br/>         | X<br/>          | X<br/> | X<br/> |
| Right<br/>        | X<br/>         | X<br/>          | X<br/> | X<br/> |
| DownRight<br/>    | -<br/>         | X<br/>          | -<br/> | X<br/> |
| RightDown<br/>    | -<br/>         | -<br/>          | X<br/> | X<br/> |
| Circle<br/>       | -<br/>         | -<br/>          | -<br/> | X<br/> |
| ChevronRight<br/> | -<br/>         | -<br/>          | -<br/> | X<br/> |



 

Microsoft s’engage à développer les *gestes*. Microsoft reconnaît que dans la création d’applications, les éditeurs de logiciels indépendants doivent connaître les actions qui seront mappées aux gestes. Les [glyphes non implémentés](unimplemented-glyphs.md) répertorient un ensemble d’actions de stylet que Microsoft envisage de mapper aux gestes, ainsi que les gestes qui sont réservés pour les actions. Ces informations sont fournies pour vous permettre de savoir quels sont les actions et les gestes qui seront fournis à l’avenir.

en plus d’utiliser des mouvements fournis dans Microsoft Windows XP Tablet PC Edition, les applications sont libres de créer leurs propres gestes. Ces mouvements peuvent ensuite être reconnus par un module de *reconnaissance de mouvement Microsoft* créé par le développeur d’applications. Si vous envisagez d’implémenter l’un de vos propres gestes, consultez les [glyphes non implémentés](unimplemented-glyphs.md) pour éviter le chevauchement avec les gestes que Microsoft prévoit d’implémenter.

 

 




