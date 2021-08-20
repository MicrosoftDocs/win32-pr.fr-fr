---
title: Liaison d’attributs ACF
description: Spécifiez la façon dont le client se connecte au serveur pour les appels de procédure distante avec les attributs énumérés dans le tableau suivant.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL, attributs, liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32b4d53cea81ed2a69a702a1a58942834a538ffbef75cb11315dd792882bf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385225"
---
# <a name="binding-acf-attributes"></a>Liaison d’attributs ACF

Spécifiez la façon dont le client se connecte au serveur pour les appels de procédure distante avec les attributs énumérés dans le tableau suivant.



| Attribut                                                          | Usage                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Suppr**](async.md)                                             | Définit un handle qui permet à l’appelant de passer un appel asynchrone et de retourner immédiatement sans attendre les résultats, puis de se resynchroniser avec la fonction appelée pour recevoir des données une fois l’appel terminé. |
| [**\_handle automatique**](auto-handle.md)                                | Indique à MIDL de laisser le code stub contrôler automatiquement la liaison. Il s’agit de la valeur par défaut si vous ne spécifiez pas de handle de liaison.                                                                                    |
| [**handle de contexte \_ \_ noserialize**](context-handle-noserialize.md) | Garantit qu’un handle de contexte ne sera jamais sérialisé, quel que soit le comportement par défaut de l’application.                                                                                                       |
| [**\_sérialisation du handle de contexte \_**](context-handle-serialize.md)     | Garantit qu’un handle de contexte sera toujours sérialisé, quel que soit le comportement par défaut de l’application.                                                                                                       |
| [**\_handle explicite**](explicit-handle.md)                        | Permet à l’application cliente de contrôler la liaison avec un paramètre explicite dans chaque procédure.                                                                                                                      |
| [**handle implicite \_**](implicit-handle.md)                        | Spécifie un handle pour les procédures qui n’ont pas de paramètre de handle explicite. L’application cliente contrôle toujours la liaison.                                                                                |
| [**\_handle de contexte strict \_**](strict-context-handle.md)           | Garantit que les méthodes de l’interface n’acceptent que des handles de contexte qui ont été créés par une méthode de cette interface.                                                                                     |



 

 

 




