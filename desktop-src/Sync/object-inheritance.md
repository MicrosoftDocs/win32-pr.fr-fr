---
description: Lorsque vous créez un processus avec la fonction CreateProcess, vous pouvez spécifier que le processus hérite des descripteurs des objets mutex, Event, Semaphore ou Timer à l’aide de la structure des attributs de sécurité \_ .
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Héritage d'objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529304"
---
# <a name="object-inheritance"></a>Héritage d'objet

Lorsque vous créez un processus avec la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , vous pouvez spécifier que le processus hérite des descripteurs des objets mutex, Event, Semaphore ou Timer à l’aide de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Le handle hérité par le processus a le même accès à l’objet que le handle d’origine. Le handle hérité apparaît dans la table de handles du processus créé, mais vous devez communiquer la valeur du handle au processus créé. Pour ce faire, vous pouvez spécifier la valeur en tant qu’argument de ligne de commande lorsque vous appelez **CreateProcess**. Le processus créé utilise ensuite la fonction [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) pour récupérer la chaîne de ligne de commande et convertir l’argument de handle en un handle utilisable. Pour plus d’informations, consultez [Héritage](../procthread/inheritance.md).

 

 
