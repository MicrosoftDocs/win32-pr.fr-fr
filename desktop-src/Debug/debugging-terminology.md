---
description: Les termes suivants sont utilisés lors de la description du débogage.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminologie du débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950385"
---
# <a name="debugging-terminology"></a>Terminologie du débogage

Les termes suivants sont utilisés lors de la description du débogage.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Écran bleu
</dt> <dd>

Lorsque le système rencontre un problème matériel, une incohérence des données ou une erreur similaire, il peut afficher un écran bleu contenant des informations qui peuvent être utilisées pour déterminer la cause de l’erreur. Ces informations incluent le code d’arrêt et indiquent si un fichier de vidage sur incident a été créé. Elle peut également inclure une liste des pilotes chargés et une trace de la pile.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Fichier de vidage sur incident
</dt> <dd>

Vous pouvez configurer le système pour écrire des informations dans un fichier de vidage sur incident sur votre disque dur à chaque fois qu’un code d’arrêt est généré. Le fichier contient des informations que le débogueur peut utiliser pour analyser l’erreur. Ce fichier peut être aussi volumineux que la mémoire physique contenue dans l’ordinateur.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Débogueur
</dt> <dd>

Programme conçu pour aider à détecter, localiser et corriger les erreurs dans un autre programme. Elle permet au développeur de parcourir l’exécution du processus et de ses threads, d’analyser la mémoire, les variables et d’autres éléments de processus et de contexte de thread.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Mode noyau
</dt> <dd>

Mode de processeur dans lequel s’exécutent les services système et les pilotes de périphérique. Toutes les interfaces et instructions de l’UC sont disponibles, et toute la mémoire est accessible.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Fichier minidump
</dt> <dd>

Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident. Pour plus d’informations, consultez [fichiers Minidump](minidump-files.md).

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>ARRÊTER le code
</dt> <dd>

Code d’erreur qui identifie l’erreur qui a empêché le noyau du système de continuer à s’exécuter.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Fichiers de symboles
</dt> <dd>

Toutes les applications système, tous les pilotes et toutes les dll sont générés de sorte que leurs informations de débogage se trouvent dans des fichiers distincts appelés fichiers de symboles. Par conséquent, le système est plus petit et plus rapide, mais il peut toujours être débogué si les fichiers de symboles sont installés. Pour plus d’informations, consultez [fichiers de symboles](symbol-files.md).

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Mode utilisateur
</dt> <dd>

Mode de processeur dans lequel les applications s’exécutent. Un ensemble limité d’interfaces est disponible dans ce mode, et l’accès aux données système est limité.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration du débogage automatique](configuring-automatic-debugging.md)
</dt> </dl>

 

 



