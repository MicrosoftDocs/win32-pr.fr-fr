---
description: Une transaction est une série de modifications apportées à un magasin de données (par exemple, une base de données ou un système de fichiers), garantissant que toutes les exécutions ont été effectuées avec succès ou qu’elles ne doivent pas être exécutées du tout.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Message Queuing transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3282a95d4f9a3ba451e78fe4d9f17acf007b0007abea4fdb4951de9c1540383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636729"
---
# <a name="transactional-message-queuing"></a>Message Queuing transactionnel

Une *transaction* est une série de modifications apportées à un magasin de données (par exemple, une base de données ou un système de fichiers), garantissant que toutes les exécutions ont été effectuées avec succès ou qu’elles ne doivent pas être exécutées du tout. Pour implémenter une transaction, un enregistrement est conservé de l’état du magasin de données avant le début de la transaction et, en cas d’échec de l’une des modifications, la transaction retourne une erreur et l’état initial est restauré (ou annulé). Les transactions sont utilisées pour maintenir l’intégrité des données et, par conséquent, jouent un rôle important dans la programmation de logiciels métier.

Souvent, les applications peuvent être développées à l’aide d’une transaction d’entreprise ou d’un flux de travail fractionné en plusieurs transactions ou activités plus petites. Ces activités sont séparées dans le temps, puis connectées à l’aide de files d’attente de messages fiables.

1.  La première transaction implique la base de données d’entrée de commande. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) déplace le message d’une file d’attente vers une autre file d’attente, exactement une fois, à l’aide des fonctionnalités de transaction. Si la base de données est mise à jour, il y a un message dans la file d’attente. Si le message n’atteint pas la file d’attente, il est abandonné et la base de données est restaurée.
2.  Plus tard, Message Queuing découvre que le serveur est disponible. Aucune application n’interroge l’existence du serveur. Il s’agit de la deuxième transaction.
3.  La troisième transaction implique une requête de la base de données d’expédition et la mise à jour de la base de données d’expédition. Si le serveur échoue au milieu de cette transaction, la modification est annulée et le message est renvoyé à la file d’attente d’entrée. Cela garantit que l’intégrité des données et des bases de données est conservée au cours des transactions.

 

 



