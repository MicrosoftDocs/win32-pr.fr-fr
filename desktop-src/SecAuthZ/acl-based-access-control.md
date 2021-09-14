---
description: Tout comme le système utilise des descripteurs de sécurité pour contrôler l’accès aux objets sécurisables, un serveur peut utiliser des descripteurs de sécurité pour contrôler l’accès à ses objets privés. pour plus d’informations sur le modèle de sécurité Windows, consultez Access Control model.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Access Control basées sur les listes de contrôle d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013732"
---
# <a name="acl-based-access-control"></a>Access Control basées sur les listes de contrôle d’accès

Tout comme le système utilise des [descripteurs de sécurité](security-descriptors.md) pour contrôler l’accès aux objets sécurisables, un serveur peut utiliser des descripteurs de sécurité pour contrôler l’accès à ses objets privés. pour plus d’informations sur le modèle de sécurité Windows, consultez [Access Control model](access-control-model.md).

Un serveur protégé peut [créer un descripteur de sécurité](security-descriptors-for-private-objects.md) avec une liste DACL qui spécifie les types d’accès autorisés pour différents types de [confiance](trustees.md). Dans un cas simple, le serveur peut créer un descripteur de sécurité unique pour [contrôler l’accès à toutes les données et fonctionnalités du serveur](checking-access-to-private-objects.md). Pour une granularité plus fine de la protection, le serveur peut créer des descripteurs de sécurité pour chacun de ses objets privés ou pour différents types de fonctionnalités.

Par exemple, lorsqu’un client demande au serveur de créer un nouvel objet dans une base de données, le serveur peut créer un descripteur de sécurité pour le nouvel objet privé. Le serveur peut ensuite stocker le descripteur de sécurité avec l’objet privé dans la base de données. Lorsqu’un client tente d’accéder à l’objet, le serveur récupère le descripteur de sécurité pour vérifier les droits d’accès du client. Il est important de noter qu’il n’y a rien dans un descripteur de sécurité qui l’associe à l’objet ou aux fonctionnalités qu’il protège. Au lieu de cela, il revient au serveur protégé de conserver l’Association.

L’accès à l’objet privé peut également être audité. Pour obtenir une description de cet objet, consultez [auditer l’accès aux objets privés](auditing-access-to-private-objects.md) .

 

 



