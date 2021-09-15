---
title: Détails de l’implémentation WOW64
description: L’émulateur WOW64 s’exécute en mode utilisateur.
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- Windows de la programmation WOW64 64 bits, variables d’environnement
- Windows de la programmation et de l’implémentation de WOW64 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127532144"
---
# <a name="wow64-implementation-details"></a>Détails de l’implémentation WOW64

L’émulateur WOW64 s’exécute en mode utilisateur. Il fournit une interface entre la version 32 bits de Ntdll.dll et le noyau du processeur, et intercepte les appels de noyau. L’émulateur WOW64 se compose des dll suivantes :

-   Wow64.dll fournit l’infrastructure d’émulation principale et les thunks pour les fonctions de point d’entrée Ntoskrnl.exe.
-   Wow64Win.dll fournit des thunks pour les fonctions de point d’entrée Win32k.sys.
-   (x64 uniquement) Wow64Cpu.dll prend en charge l’exécution de programmes x86 sur x64.
-   (Intel Itanium uniquement) IA32Exec. bin contient l’émulateur de logiciel x86.
-   (Intel Itanium uniquement) Wowia32x.dll fournit l’interface entre IA32Exec. bin et WOW64.
-   (ARM64 uniquement) xtajit.dll contient l’émulateur de logiciel x86.
-   (ARM64 uniquement) wowarmw.dll prend en charge l’exécution de programmes ARM32 sur ARM64.

Ces dll, ainsi que la version 64 bits de Ntdll.dll, sont les seuls binaires 64 bits qui peuvent être chargés dans un processus 32 bits. sur Windows 10 sur ARM, les fichiers binaires CHPE (fichier exécutable hybride hybride compilé) peuvent également être chargés dans un processus x86 32 bits.

Au démarrage, Wow64.dll charge la version x86 de Ntdll.dll (ou la version CHPE, si elle est activée) et exécute son code d’initialisation, qui charge toutes les dll 32 bits nécessaires. presque toutes les dll 32 bits sont des copies non modifiées des binaires de Windows 32 bits, bien que certaines soient chargées en tant que CHPE pour des raisons de performances. certaines de ces dll sont écrites pour se comporter différemment sur WOW64 et sur les Windows 32 bits, généralement parce qu’elles partagent la mémoire avec les composants système de 64 bits. Tout l’espace d’adressage en mode utilisateur au-dessus de la limite de 32 bits est réservé par le système. Pour plus d’informations, consultez [consommation de performances et de mémoire sous WOW64](performance-and-memory-consumption.md).

Au lieu d’utiliser la séquence d’appels du service système x86, les binaires 32 bits qui effectuent des appels système sont reconstruits pour utiliser une séquence d’appel personnalisée. Cette séquence d’appel est peu coûteuse pour que WOW64 soit interceptée, car elle reste entièrement en mode utilisateur. Lorsque la séquence d’appel personnalisée est détectée, l’UC WOW64 passe en mode natif 64 bits et appelle Wow64.dll. Le thunking est effectué en mode utilisateur pour réduire l’impact sur le noyau 64 bits et pour réduire le risque d’un bogue dans le thunk qui peut provoquer un incident en mode noyau, une altération des données ou une brèche de sécurité. Les thunks extraient les arguments de la pile 32 bits, les étendent à 64 bits, puis effectuent l’appel système natif.

## <a name="environment-variables"></a>Variables d'environnement

Quand un processus 32 bits est créé par un processus 64 bits, ou lorsqu’un processus 64 bits est créé par un processus de 32 bits, WOW64 définit les variables d’environnement pour le processus créé, comme indiqué dans le tableau suivant.



| Process                   | Variables d'environnement                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| processus 64 bits<br/> | Architecture du processeur \_ = amd64 ou \_ architecture du processeur = IA64 ou architecture du processeur \_ = ARM64<br/> ProgramFiles =% ProgramFiles%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/> **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** les variables d’environnement ProgramW6432 et CommonProgramW6432 ont été ajoutées à partir de Windows 7 et Windows Server 2008 R2. <br/> |
| processus 32 bits<br/> | ARCHITECTURE du processeur \_ = x86<br/> PROCESSEUR \_ ARCHITEW6432 =% \_ architecture processeur%<br/> ProgramFiles =% ProgramFiles (x86)%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles (x86)%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>Raccordements globaux

La fonction [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) peut être utilisée pour injecter une dll dans un autre processus si les conditions suivantes sont remplies :

-   Une DLL 32 bits peut être injectée uniquement dans un processus 32 bits et une DLL 64 bits ne peut être injectée que dans un processus de 64 bits. Il n’est pas possible d’injecter une DLL 32 bits dans un processus 64 bits ou vice versa.
-   Les dll 32 bits et 64 bits doivent avoir des noms différents.
-   Les architectures de la DLL et du processus doivent correspondre. Par exemple, vous ne pouvez pas injecter une DLL x86 32 bits dans un processus ARM 32 bits.

Pour plus d’informations, consultez [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).

N’oubliez pas que l’interpréteur de commandes de la **\_ souris**, du **\_ clavier**, du **Journal _ et du \_ \* \_ Shell *_* WH** et des crochets de bas niveau peut être appelé sur le thread qui a installé le hook plutôt que sur le thread traitant le hook. Pour ces raccordements, il est possible que les crochets 32 bits et 64 bits soient appelés si un hook 32 bits est avant un hook 64 bits dans la chaîne de raccordement. Pour plus d’informations, consultez [utilisation de hooks](../winmsg/using-hooks.md).

 

