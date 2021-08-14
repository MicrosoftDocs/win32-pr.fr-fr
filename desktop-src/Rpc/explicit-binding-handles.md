---
title: Handles de liaison explicites
description: Pour un contrôle maximal sur le processus de liaison, les applications client/serveur peuvent utiliser des handles de liaison explicites.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a6e723d8559dc5e72783412eb6250f69431f31d08a92c4984fb2e2a19b761d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930018"
---
# <a name="explicit-binding-handles"></a>Handles de liaison explicites

Pour un contrôle maximal sur le processus de liaison, les applications client/serveur peuvent utiliser des handles de liaison explicites. À l’instar des handles implicites, les handles de liaison explicites permettent à votre application cliente de sélectionner un serveur pour exécuter ses appels. En outre, les handles de liaison explicites permettent à votre application client/serveur de créer une session de communication RPC authentifiée. Avec les handles explicites, votre client peut se connecter à plusieurs serveurs et exécuter des procédures distantes sur plusieurs serveurs. Les applications clientes multithread et asynchrones peuvent même se connecter à plusieurs serveurs et exécuter plusieurs procédures distantes en même temps.

Votre application cliente doit passer le handle explicite en tant que paramètre à chaque appel de procédure distante. Pour se conformer à la norme OSF, le descripteur doit être spécifié en tant que premier paramètre sur chaque procédure distante. Toutefois, les extensions Microsoft de RPC vous permettent de spécifier le descripteur de liaison dans d’autres positions. Pour plus d’informations, consultez [Microsoft RPC Binding-Handle extensions](microsoft-rpc-binding-handle-extensions.md).

Pour créer un handle explicite, déclarez le descripteur en tant que paramètre pour les opérations distantes dans le fichier IDL. L' [exemple Hello, World](tutorial.md) peut être redéfini pour utiliser un handle explicite comme indiqué ci-dessous :

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

Vous pouvez combiner des handles explicites et implicites dans une seule interface. Si une fonction a un handle explicite dans sa liste de paramètres, ce handle sera utilisé. Si une fonction dans une interface utilisant des handles implicites ne spécifie pas de handle explicite, le handle implicite par défaut sera utilisé.

 

 




