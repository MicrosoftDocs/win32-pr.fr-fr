---
title: Comment les clients composent le SPN d’un service
description: Pour authentifier un service, une application cliente compose un SPN pour l’instance de service à laquelle il doit se connecter.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Comment les clients composent la publicité SPN d’un service
- nom de principal du service AD, comment les clients composent le SPN d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06c3531ac329af1a4c4fa7721b5d575ce762d86f15767278ad9a348e7956cfa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188184"
---
# <a name="how-clients-compose-a-services-spn"></a>Comment les clients composent le SPN d’un service

Pour authentifier un service, une application cliente compose un SPN pour l’instance de service à laquelle il doit se connecter. L’application cliente peut utiliser la fonction [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) pour composer un SPN. Le client spécifie les composants du SPN à l’aide de données connues ou de données récupérées à partir de sources autres que le service lui-même.

Le format d’un SPN est le suivant :


```C++
<service class>/<host>:<port>/<service name>
```



Dans ce formulaire, « &lt; classe &gt; de service » et « &lt; hôte &gt; » sont requis. « &lt; port &gt; » et « &lt; nom du service &gt; » sont facultatifs.

En règle générale, le client reconnaît la &lt; partie « classe &gt; de service » du nom et reconnaît les composants facultatifs à inclure dans le SPN. Le client peut récupérer des composants du SPN à partir de sources telles qu’un point de connexion de service (SCP) ou une entrée d’utilisateur. Par exemple, le client peut lire l’attribut **servicednsname** du SCP d’un service pour obtenir le &lt; composant « host &gt; ». L’attribut **servicednsname** contient soit le nom DNS du serveur sur lequel s’exécute l’instance de service, soit le nom DNS des enregistrements SRV contenant les données d’hôte pour les réplicas de service. Le &lt; composant « nom du service &gt; », utilisé uniquement pour les services réplicables, peut être le nom unique du SCP du service, le nom DNS du domaine pris en charge par le service ou le nom DNS des enregistrements SRV ou MX.

pour plus d’informations et pour obtenir un exemple de code utilisé pour composer un SPN pour un service, consultez [comment un Client authentifie un service de sockets Windows basé sur SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Pour plus d’informations et pour obtenir une description des composants SPN, consultez [formats de noms pour les noms de](name-formats-for-unique-spns.md)principal du service uniques.

 

 




