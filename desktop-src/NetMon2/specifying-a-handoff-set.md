---
description: Un jeu de remise spécifie les protocoles qui suivent un protocole. L’analyseur utilise un jeu de remise uniquement lorsque l’analyseur peut identifier le protocole suivant à partir des données dans une instance de protocole.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Spécification d’un jeu de remise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f3f7d559c83e3c56bc6ea202b3a0e339dbc1b76d93fc2af1b73f5a2c60c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778349"
---
# <a name="specifying-a-handoff-set"></a>Spécification d’un jeu de remise

Un jeu de remise spécifie les protocoles qui suivent un protocole. L’analyseur utilise un jeu de remise uniquement lorsque l’analyseur peut identifier le protocole suivant à partir des données dans une instance de protocole.

Par exemple, le protocole TCP a une propriété port qui identifie le protocole qui suit le protocole TCP. Une valeur de propriété de 20 indique que le protocole suivant est FTP. Une valeur de propriété de 53 indique que le protocole suivant est DNS. Étant donné que la propriété port identifie le protocole qui suit, l’analyseur TCP peut utiliser le jeu de remise suivant pour obtenir un descripteur pour le protocole que la propriété Port spécifie.

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

Les jeux de remise sont stockés dans le fichier INI de l’analyseur. Par exemple, le jeu de remise TCP précédent se trouve dans tcpip.ini fichier. Notez que si une DLL de l’analyseur prend en charge plusieurs protocoles, chaque analyseur qui utilise un jeu de remise a son propre emplacement dans le fichier INI.

Les informations de jeu de remise sont spécifiées lors de l’implémentation de la fonction [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . L’analyseur peut spécifier les protocoles qui précèdent le protocole de l’analyseur et les protocoles qui suivent le protocole de l’analyseur. Moniteur réseau prend tous les protocoles qui précèdent et ajoute le protocole d’analyse aux sections de l’ensemble suivant du fichier INI de l’analyseur, pour chaque protocole précédent. Moniteur réseau stocke la liste des protocoles qui suivent dans la section du jeu de remise du fichier INI de l’analyseur.

Moniteur réseau stocke les informations du jeu de remise dans le fichier INI de l’analyseur, mais l’analyseur n’accède pas directement aux fichiers INI. Pour utiliser les informations du jeu de remise, l’analyseur appelle la fonction [**CreateHandoffTable**](createhandofftable.md) pour créer une table de remise. En règle générale, la table de remise est créée lorsque l’analyseur enregistre le protocole. Une fois le protocole inscrit, Moniteur réseau crée une table de jeu de remise que l’analyseur peut utiliser.

L’analyseur utilise son jeu de remise lors de la reconnaissance des données. Tout d’abord, l’analyseur lit la valeur de la propriété qui identifie le protocole suivant. L’analyseur appelle ensuite [**GetProtocolFromTable**](getprotocolfromtable.md) pour obtenir un handle vers le protocole suivant. Enfin, l’analyseur retourne un pointeur vers le descripteur dans le paramètre *phNextProtocol* de [**RecognizeFrame**](recognizeframe.md).

 

 



