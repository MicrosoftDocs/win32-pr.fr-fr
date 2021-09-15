---
title: attribut de chaîne (RPC)
description: L’attribut \ String \ et l’appel de procédure distante (RPC).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413494"
---
# <a name="string-attribute-rpc"></a>attribut de chaîne (RPC)

L' \[ [](/windows/desktop/Midl/string) \] attribut String indique que le paramètre est un pointeur vers un tableau de type [char](/windows/desktop/Midl/char-idl), [Byte](/windows/desktop/Midl/byte)ou **w \_ char**. Comme avec un tableau conforme, la taille d’un paramètre de **\[ chaîne \]** est déterminée au moment de l’exécution. Contrairement à un tableau conforme, le développeur n’a pas besoin de fournir la longueur associée au tableau. l’attribut de **\[ \] chaîne** indique au stub de déterminer la taille du tableau en appelant **strlen**. Un attribut de **\[ \] chaîne** ne peut pas être utilisé en même temps que la \[ [longueur \_](/windows/desktop/Midl/length-is) ou est le \] \[ [dernier \_](/windows/desktop/Midl/last-is) \] attribut.

Dans, la combinaison d’attributs **\[ de chaîne \]** indique au stub de passer la chaîne du client au serveur uniquement. La quantité de mémoire allouée sur le serveur est identique à la taille de chaîne transmise plus un.

Les \[ attributs de **chaîne** [out](/windows/desktop/Midl/out-idl) \] indiquent au stub de passer la chaîne du serveur au client uniquement. La conception appel par valeur du langage C insiste sur le faire que tous les paramètres de **\[ sortie \]** doivent être des pointeurs.

Le paramètre de **\[ sortie \]** doit être un pointeur et, par défaut, tous les paramètres de pointeur sont des pointeurs de référence. Le pointeur de référence ne change pas pendant l’appel, il pointe vers la même mémoire que celle avant l’appel. Pour les pointeurs de chaîne, la contrainte supplémentaire du pointeur de référence signifie que le client doit allouer suffisamment de mémoire valide avant d’effectuer l’appel de procédure distante. Les stubs transmettent la chaîne que les attributs **\[ out, String \]** indiquent dans la mémoire déjà allouée côté client.

Les rubriques suivantes décrivent les prototypes de paramètre de procédure distante pour les chaînes :

-   [\[in, out, prototype de chaîne \]](-in-out-string-prototype.md)
-   [\[in, String \] et \[ out, prototype de chaîne \]](-in-string-and-out-string-prototype.md)

 

 