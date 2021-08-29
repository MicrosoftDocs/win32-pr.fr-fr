---
description: La fiabilité d’un certificat numérique est établie à l’aide d’une hiérarchie d’approbation.
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: Hiérarchie d’approbation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67955c9dc94c09cf391f58375ae00f74a1584d536ad299bb2f5d1335dd1aeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006234"
---
# <a name="hierarchy-of-trust"></a>Hiérarchie d’approbation

Pour que les [*certificats numériques*](../secgloss/c-gly.md) soient efficaces, les utilisateurs de certificats doivent disposer d’un niveau de confiance élevé. Dans certains cas, un utilisateur ne fait pas confiance à l’émetteur d’un certificat. Cela peut se produire si l’utilisateur du certificat n’a jamais entendu parler de l' [*autorité de certification*](../secgloss/c-gly.md) et n’a donc pas l’habitude d’accepter un certificat de cet émetteur à la valeur faciale. Ce problème est résolu dans le processus de certification par une hiérarchie d’approbation.

Une hiérarchie d’approbation commence par au moins une autorité de certification approuvée par toutes les entités dans la chaîne de certificats. Il peut s’agir d’un administrateur d’autorité de certification interne ou d’une société ou organisation externe spécialisée dans la vérification des identités et l’émission de certificats. Cette autorité est appelée [*autorité racine*](../secgloss/r-gly.md). L’autorité racine certifie ensuite d’autres autorités de certification, appelées autorités de certification de première couche, qui peuvent émettre des certificats et également certifier des autorités de certification supplémentaires ou de deuxième niveau. Cette situation est présentée dans l’illustration suivante.

![hiérarchie d’approbation](images/trust.png)

L’identité de l’autorité de certification qui émet un certificat fait partie d’un certificat. Cette autorité de certification est appelée émetteur du certificat. Lorsque l’émetteur d’un certificat est une autorité de certification de niveau 1 ou 2, le destinataire de ce certificat peut déterminer si l’émetteur du certificat est certifié en tant qu’autorité de certification valide par une autorité de certification à un niveau supérieur, et que l’autorité de certification de niveau supérieur est certifiée en tant qu’autorité de certification valide par une autorité de certification de niveau supérieur jusqu’à ce qu’il soit déterminé qu’une chaîne d’approbation existe entre le niveau le plus bas. autorité de certification et autorité de certification racine.

Par exemple, dans l’illustration précédente, il est possible de vérifier que l’autorité de certification \# 4 a été certifiée en tant qu’autorité de certification par l’autorité de certification \# 1, et que l’autorité de certification \# 1 a été certifiée en tant qu’autorité de certification par l’autorité de certification racine. Ainsi, lorsqu’un certificat d’une autorité de certification de niveau inférieur est transmis avec le message chiffré, les informations sur tous les certificats de sa chaîne de confiance jusqu’à la racine sont transmises.

L’illustration et la description que vous venez de présenter sont conceptuelles. Dans le monde réel, la situation de l’autorité de certification évolue et aucune autorité racine unique n’a été établie ou acceptée. À bref terme, les îles de l’autorité se développeront comme indiqué dans l’illustration suivante.

![îles d’autorité dans une hiérarchie d’approbation](images/trust2.png)

Dans le temps, les îlots racines, root 1 et root 2 de l’illustration, pouvaient devenir des autorités de certification de niveau 1 à une autorité de certification racine unique. À ce stade, la situation aurait une seule autorité racine. Il reste à voir exactement comment l’image réelle va évoluer.

 

 
