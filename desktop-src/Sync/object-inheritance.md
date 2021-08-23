---
description: Lorsque vous créez un processus avec la fonction CreateProcess, vous pouvez spécifier que le processus hérite des descripteurs des objets mutex, Event, Semaphore ou Timer à l’aide de la structure des attributs de sécurité \_ .
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Héritage d'objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661379"
---
# <a name="object-inheritance"></a>Héritage d'objet

Lorsque vous créez un processus avec la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , vous pouvez spécifier que le processus hérite des descripteurs des objets mutex, Event, Semaphore ou Timer à l’aide de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Le handle hérité par le processus a le même accès à l’objet que le handle d’origine. Le handle hérité apparaît dans la table de handles du processus créé, mais vous devez communiquer la valeur du handle au processus créé. Pour ce faire, vous pouvez spécifier la valeur en tant qu’argument de ligne de commande lorsque vous appelez **CreateProcess**. Le processus créé utilise ensuite la fonction [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) pour récupérer la chaîne de ligne de commande et convertir l’argument de handle en un handle utilisable. Pour plus d’informations, consultez [Héritage](../procthread/inheritance.md).

 

 
