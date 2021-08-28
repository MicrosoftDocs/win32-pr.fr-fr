---
title: Débogage de WOW64
description: Les applications qui s’exécutent sous WOW64 peuvent être déboguées à l’aide d’un débogueur hébergé par x86 ou d’un débogueur natif.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- programmation Windows WOW64 64 bits, débogage
- débogage de la programmation Windows WOW64 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa0f101f382239d146cf668e46efc245753f86ec3c876087f9a4a94bbd356f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121809"
---
# <a name="debugging-wow64"></a>Débogage de WOW64

Les applications qui s’exécutent sous WOW64 peuvent être déboguées de deux manières :

-   Utilisez un débogueur hébergé sur x86, tel que NTSD, WinDbg ou Visual Studio. Le NTSD 32 bits est installé dans% SystemRoot% \\ SysWOW64 sur les installations de vente au détail. Notez que les débogueurs x86 peuvent être utilisés pour déboguer du code x86, mais ne peuvent pas être utilisés pour désassembler ou définir des points d’arrêt dans la couche du thunk WOW64, car il s’agit d’un code natif 64 bits.
-   Utilisez un débogueur natif tel que CDB, NTSD ou WinDbg et l’extension de débogueur WOW64, Wow64exts.dll. Si le débogueur natif s’arrête alors que le processeur est en mode x86, le débogueur présente le processus en tant que processus x86. Si le processeur est en mode natif, le débogueur présente le processus comme natif.

CDB, NTSD et WinDbg sont inclus dans les outils de débogage pour Windows. pour plus d’informations, consultez la documentation [sur les outils de débogage pour Windows](/windows-hardware/drivers/debugger/) .

L’extension du débogueur Wow64exts est installée avec WinDbg. Utilisez la commande ! Load wow64exts pour charger l’extension du débogueur. Le tableau suivant répertorie les commandes d’extension du débogueur ! wow64exts.



| Commande                | Description                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ! wow64exts. SW          | Bascule entre le mode x86 et le mode natif.                                                                                                    |
| ! wow64exts. k *Count*   | Vide une trace de la pile 32 bits/64 bits combinée. Si *Count* est spécifié, la commande vide *les premières adresses* de chaque trace de la pile.  |
| ! wow64exts.info        | Vide les informations de base sur le PEB du processus, le TEB du thread actuel et les emplacements de stockage local des threads (TLS) utilisés par WOW64. |
| ! wow64exts. r *adresse* | Fait un dump du contexte pour l’adresse spécifiée. Si *Address* n’est pas spécifié, la commande vide le contexte pour le processeur.                     |



 

 

 