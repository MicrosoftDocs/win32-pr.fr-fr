---
title: Utiliser des handles de contexte pour conserver l’État sur le serveur
description: Utiliser des handles de contexte pour conserver l’État sur le serveur
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9360d4edf95c06cef30a0e07f0e541a89823e89b163d5bbb61e0fb686a4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010957"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a>Utiliser des handles de contexte pour conserver l’État sur le serveur

**Bonne pratique :** Chaque fois que l’État est conservé sur le serveur entre les appels, utilisez des handles de contexte.

Les handles de contexte sont souvent intimidants pour les nouveaux programmeurs RPC, et la surcharge des handles de contexte d’apprentissage n’est peut-être pas initialement la peine d’être consentie. C’est la raison pour laquelle les descripteurs de contexte ont des solutions intégrées pour de nombreux pièges courants rencontrés dans la programmation réseau qui devraient normalement être implémentés à partir de zéro. La compréhension des handles de contexte paye les dividendes ultérieurement.

 

 




