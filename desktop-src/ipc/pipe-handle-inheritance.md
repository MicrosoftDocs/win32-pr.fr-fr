---
description: Le serveur de canaux contrôle si ses Handles peuvent être hérités des manières suivantes.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Héritage de handle de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cf91d4393b43011a2df632806f96da1e713b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749669"
---
# <a name="pipe-handle-inheritance"></a>Héritage de handle de canal

Le serveur de canaux contrôle si ses Handles peuvent être hérités des manières suivantes :

-   La fonction [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) reçoit une structure d' [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Si le serveur de canal affecte la **valeur true** au membre **bInheritHandle** de cette structure, les descripteurs créés par **CreatePipe** peuvent être hérités.
-   Le serveur de canal peut utiliser la fonction [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) pour modifier l’héritage d’un handle de canal. Le serveur de canaux peut créer un doublon non héritable d’un handle de canal héritable ou un doublon pouvant être hérité d’un handle de canal non héritable.
-   La fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) permet au serveur de canal de spécifier si un processus enfant hérite de tout ou partie de ses Handles pouvant être hérités.

Lorsqu’un processus enfant hérite d’un handle de canal, le système permet au processus d’accéder au canal. Toutefois, le processus parent doit communiquer la valeur du handle au processus enfant. Le processus parent effectue généralement cette opération en redirigeant le descripteur de sortie standard vers le processus enfant, comme indiqué dans les étapes suivantes :

1.  Appelez la fonction [**GetStdHandle**](/windows/console/getstdhandle) pour récupérer le handle de sortie standard actuel ; Enregistrez ce handle pour pouvoir restaurer le descripteur de sortie standard d’origine après la création du processus enfant.
2.  Appelez la fonction [**SetStdHandle**](/windows/console/setstdhandle) pour définir le handle de sortie standard du handle d’écriture sur le canal. Désormais, le processus parent peut créer le processus enfant.
3.  Appelez la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) pour fermer le handle d’écriture sur le canal. Une fois que le processus enfant hérite du handle d’écriture, le processus parent n’a plus besoin de sa copie.
4.  Appelez [**SetStdHandle**](/windows/console/setstdhandle) pour restaurer le descripteur de sortie standard d’origine.

Le processus enfant utilise la fonction [**GetStdHandle**](/windows/console/getstdhandle) pour obtenir son descripteur de sortie standard, qui est maintenant un handle vers la fin d’écriture d’un canal. Le processus enfant utilise ensuite la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) pour envoyer sa sortie vers le canal. Lorsque l’enfant a terminé avec le canal, il doit fermer le handle de canal en appelant [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) ou en terminant, ce qui ferme automatiquement le handle.

Le processus parent utilise la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) pour recevoir l’entrée du canal. Les données sont écrites dans un canal anonyme en tant que flux d’octets. Cela signifie que le processus parent lisant à partir d’un canal ne peut pas faire la distinction entre les octets écrits dans des opérations d’écriture distinctes, à moins que les processus parent et enfant utilisent un protocole pour indiquer l’emplacement de fin de l’opération d’écriture. Lorsque tous les descripteurs d’écriture du canal sont fermés, la fonction **ReadFile** retourne la valeur zéro. Il est important que le processus parent ferme son handle à la fin d’écriture du canal avant d’appeler **ReadFile**. Si ce n’est pas le cas, l’opération **ReadFile** ne peut pas retourner la valeur zéro, car le processus parent a un handle ouvert à la fin d’écriture du canal.

La procédure de redirection du handle d’entrée standard est semblable à celle utilisée pour rediriger le descripteur de sortie standard, à la différence près que le handle de lecture du canal est utilisé comme handle d’entrée standard de l’enfant. Dans ce cas, le processus parent doit s’assurer que le processus enfant n’hérite pas du handle d’écriture du canal. Si ce n’est pas le cas, l’opération [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) effectuée par le processus enfant ne peut pas retourner la valeur zéro, car le processus enfant a un handle ouvert à la fin d’écriture du canal.

Pour obtenir un exemple de programme qui utilise des canaux anonymes pour rediriger les handles standard d’un processus enfant, consultez [création d’un processus enfant avec une entrée et une sortie redirigées](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output).

 

 
