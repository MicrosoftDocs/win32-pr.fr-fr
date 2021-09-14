---
description: Un jeu suivant spécifie les protocoles qui suivent un protocole. Moniteur réseau utilise un jeu de suivi lorsque l’analyseur ne parvient pas à identifier le protocole suivant à partir des données dans une instance de protocole.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Spécification d’un jeu de suivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194543"
---
# <a name="specifying-a-follow-set"></a>Spécification d’un jeu de suivi

Un jeu suivant spécifie les protocoles qui suivent un protocole. Moniteur réseau utilise un jeu de suivi lorsque l’analyseur ne parvient pas à identifier le protocole suivant à partir des données dans une instance de protocole.

Par exemple, l’analyseur NetBIOS spécifie un jeu de suivi, car les données du protocole NetBIOS n’identifient pas le protocole suivant. Par conséquent, l’analyseur NetBIOS doit créer un ensemble de tous les protocoles qui peuvent être suivis.

L’exemple de code suivant identifie le jeu de suivi NetBIOS dans le fichier [*Parser.ini*](p.md) . Le jeu suivant contient les protocoles SMB (Server Message Block) et MSRPC (Microsoft Remote Procedure Call). Il s’agit des seuls protocoles qui peuvent suivre une instance du protocole NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Un analyseur spécifie un jeu de suivi lors de l’implémentation de la fonction [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . Un analyseur peut spécifier quels protocoles précèdent et quels protocoles suivent. Lorsqu’un analyseur spécifie les protocoles qui précèdent, Moniteur réseau ajoute le protocole d’analyseur aux ensembles suivants des protocoles spécifiés. Lorsqu’un analyseur spécifie les protocoles qui suivent, Moniteur réseau crée une nouvelle section dans le fichier Parser.ini qui comprend le jeu suivant de l’analyseur.

 

 



