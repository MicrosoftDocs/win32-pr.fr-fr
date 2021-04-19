---
description: Un processus enfant peut hériter de handles de son processus parent. Un handle hérité est valide uniquement dans le contexte du processus enfant. Pour permettre à un processus enfant d’hériter des handles ouverts de son processus parent, procédez comme suit.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Gérer l’héritage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545088"
---
# <a name="handle-inheritance"></a>Gérer l’héritage

Un processus enfant peut hériter de handles de son processus parent. Un handle hérité est valide uniquement dans le contexte du processus enfant. Pour permettre à un processus enfant d’hériter des handles ouverts de son processus parent, procédez comme suit.

1.  Créez le descripteur avec le membre **bInheritHandle** de la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) défini sur **true**.
2.  Créez le processus enfant à l’aide de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , avec le paramètre *BInheritHandles* défini sur **true**.

La fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) duplique un handle à utiliser dans le processus en cours ou dans un autre processus. Si une application duplique l’un de ses descripteurs pour un autre processus, le handle dupliqué est valide uniquement dans le contexte de l’autre processus.

Un handle dupliqué ou un handle hérité est une valeur unique, mais il fait référence au même objet que le handle d’origine. Les processus peuvent hériter ou dupliquer des handles vers les types d’objets suivants :

-   Jeton d'accès
-   Appareil de communication
-   Entrée de la console
-   Mémoire tampon d’écran de la console
-   Bureau
-   Répertoire
-   Événement
-   Fichier
-   Mappage de fichiers
-   Travail
-   Mailslots
-   Mutex
-   Pipe
-   Process
-   Clé de Registre
-   Semaphore
-   Prise
-   Thread
-   Minuteur
-   Station Windows

Tous les autres objets sont privés pour le processus qui les a créés ; leurs handles d’objet ne peuvent pas être dupliqués ou hérités.

Pour plus d’informations, consultez [Héritage](/windows/desktop/ProcThread/inheritance).

 

 
