---
description: Lorsqu’un nouveau thread est créé par la fonction CreateThread ou CreateRemoteThread, un descripteur du thread est retourné.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Handles et identificateurs de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6058388f450b4b44c371fc26b132ea785b22c29bc0a2fd86875f563371608512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031629"
---
# <a name="thread-handles-and-identifiers"></a>Handles et identificateurs de thread

Lorsqu’un nouveau thread est créé par la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) , un descripteur du thread est retourné. Par défaut, ce handle dispose de droits d’accès complets et, sous réserve de la vérification de l’accès à la sécurité, peut être utilisé dans toutes les fonctions qui acceptent un handle de thread. Ce handle peut être hérité par les processus enfants, en fonction de l’indicateur d’héritage spécifié lors de sa création. Le descripteur peut être dupliqué par [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle), ce qui vous permet de créer un handle de thread avec un sous-ensemble des droits d’accès. Le handle est valide jusqu’à la fermeture, même après l’arrêt du thread qu’il représente.

Les fonctions [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) et [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) retournent également un identificateur qui identifie de façon unique le thread dans l’ensemble du système. Un thread peut utiliser la fonction [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) pour obtenir son propre identificateur de thread. Les identificateurs sont valides à partir du moment où le thread est créé jusqu’à l’arrêt du thread. Notez qu’aucun identificateur de thread ne sera jamais égal à 0.

Si vous avez un identificateur de thread, vous pouvez obtenir le handle de thread en appelant la fonction [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) . **OpenThread** vous permet de spécifier les droits d’accès du handle et s’il peut être hérité.

Un thread peut utiliser la fonction [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) pour récupérer un *Pseudo-handle* vers son propre objet thread. Ce pseudo-handle est valide uniquement pour le processus appelant ; elle ne peut pas être héritée ou dupliquée pour être utilisée par d’autres processus. Pour obtenir le handle réel du thread, étant donné un pseudo handle, utilisez la fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

Pour énumérer les threads d’un processus, utilisez les fonctions [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) et [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) .

 

 
