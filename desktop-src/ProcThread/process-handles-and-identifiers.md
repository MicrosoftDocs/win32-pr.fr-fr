---
description: Lorsqu’un nouveau processus est créé par la fonction CreateProcess, les handles du nouveau processus et son thread principal sont retournés.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Handles et identificateurs de processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007104"
---
# <a name="process-handles-and-identifiers"></a>Handles et identificateurs de processus

Lorsqu’un nouveau processus est créé par la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) , les handles du nouveau processus et son thread principal sont retournés. Ces handles sont créés avec des droits d’accès complets et, sous réserve de la vérification de l’accès de sécurité, peuvent être utilisés dans n’importe quelle fonction qui accepte les handles de thread ou de processus. Ces handles peuvent être hérités par les processus enfants, en fonction de l’indicateur d’héritage spécifié lors de leur création. Les handles sont valides jusqu’à la fermeture, même après la fin du processus ou du thread qu’ils représentent.

La fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) retourne également un identificateur qui identifie de façon unique le processus dans le système. Un processus peut utiliser la fonction [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) pour obtenir son propre identificateur de processus (également appelé ID de processus ou PID). L’identificateur est valide à partir de l’heure à laquelle le processus est créé jusqu’à ce que le processus soit arrêté. Un processus peut utiliser la fonction [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) pour obtenir l’identificateur de processus de son processus parent.

Si vous avez un identificateur de processus, vous pouvez obtenir le handle de processus en appelant la fonction [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) . **OpenProcess** vous permet de spécifier les droits d’accès du handle et s’il peut être hérité.

Un processus peut utiliser la fonction [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) pour récupérer un pseudo-handle vers son propre objet Process. Ce pseudo-handle est valide uniquement pour le processus appelant ; elle ne peut pas être héritée ou dupliquée pour être utilisée par d’autres processus. Pour récupérer le handle réel du processus, appelez la fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

 

 
