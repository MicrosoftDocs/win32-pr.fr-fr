---
title: Sérialisation de type
description: Le compilateur MIDL génère jusqu’à trois fonctions pour chaque type auquel l’attribut \ encode \ ou \ Decode \ est appliqué.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d898a077ff55bb03a76fbd7579e28a8bcdf18c792330b32b1eb832c6b9058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011097"
---
# <a name="type-serialization"></a>Sérialisation de type

Le compilateur MIDL génère jusqu’à trois fonctions pour chaque type auquel l’attribut \[ [encode](/windows/desktop/Midl/encode) \] ou \[ [Decode](/windows/desktop/Midl/decode) \] est appliqué. Par exemple, pour un type défini par l’utilisateur nommé *MyType*, le compilateur génère du code pour les \_ fonctions de décodage MyType, MyType \_ et MyType \_ AlignSize. Pour ces fonctions, le compilateur écrit les prototypes dans stub. h et le code source dans le stub \_ c.c. En général, vous pouvez encoder un objet *MyType* avec MyType \_ encode et décoder un objet à partir de la mémoire tampon à l’aide du \_ décodage MyType. MyType \_ AlignSize est utilisé si vous avez besoin de connaître la taille de la mémoire tampon de marshaling avant de l’allouer.

La fonction d’encodage suivante est générée par le compilateur MIDL. Cette fonction sérialise les données pour l’objet pointé par pObject, et la mémoire tampon est obtenue en fonction de la méthode spécifiée dans le handle. Après avoir écrit les données sérialisées dans la mémoire tampon, vous contrôlez la mémoire tampon. Notez que le handle hérite de l’état des appels précédents et que les mémoires tampons doivent être alignées sur 8.

Pour un handle implicite :

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Pour un handle explicite :

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La fonction suivante désérialise les données du stockage de l’application dans l’objet désigné par pObject. Vous fournissez une mémoire tampon marshalée en fonction de la méthode spécifiée dans le handle. Notez que le handle peut hériter de l’état des appels précédents et que les mémoires tampons doivent être alignées sur 8.

Pour un handle implicite :

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Pour un handle explicite :

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La fonction suivante retourne une taille, en octets, qui comprend l’instance de type plus les octets de remplissage nécessaires à l’alignement des données. Cela permet de sérialiser un jeu d’instances de types identiques ou différents dans une mémoire tampon tout en veillant à ce que les données de chaque objet soient correctement alignées. MyType \_ AlignSize suppose que l’instance vers laquelle pointe pObject est marshalée dans une mémoire tampon en commençant au décalage aligné à 8.

Pour un handle implicite :

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Pour un handle explicite :

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Notez que les procédures distantes avec des handles de liaison implicites et des types sérialisés avec des handles de sérialisation implicites utilisent la même variable de handle globale. Par conséquent, il est recommandé de ne pas mélanger la sérialisation de type et les procédures distantes dans une interface avec des handles implicites. Pour plus d’informations, consultez [Handles implicites et Handles explicites](implicit-versus-explicit-handles.md).

 

 