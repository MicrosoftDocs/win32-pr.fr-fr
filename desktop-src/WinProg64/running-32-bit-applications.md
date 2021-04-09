---
title: Exécution d’applications 32 bits
description: Exécutez des applications Windows 32 bits en toute transparence sur Windows 64 bits avec l’émulateur WOW64 x86. En savoir plus sur le directeur du Registre, le redirecteur du système de fichiers, l’installation des applications sur les systèmes 64 bits et le débogage de WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- WOW64 (programmation Windows) 64 bits
- WOW64, programmation Windows 64 bits, à propos de
- applications 32 bits 64 sur la programmation Windows 64 bits Windows bits
- Guide de programmation Windows 64 bits sur la programmation Windows 64 bits, WOW64 voir WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941044"
---
# <a name="running-32-bit-applications"></a>Exécution d’applications 32 bits

WOW64 est l’émulateur x86 qui permet aux applications basées sur Windows 32 bits de s’exécuter de façon transparente sur Windows 64 bits. Cela permet aux applications Windows 32 bits (x86) de s’exécuter en toute transparence dans Windows 64 bits (x64), ainsi que pour les applications Windows 32 bits (x86) et 32 bits pour s’exécuter en toute transparence dans Windows 64-bit (ARM64). WOW64 est fourni avec le système d’exploitation et n’a pas besoin d’être explicitement activé. Pour plus d’informations, consultez détails de l' [implémentation WOW64](wow64-implementation-details.md).

Le système isole les applications 32 bits des applications 64 bits, ce qui comprend la prévention des collisions de fichiers et de registres. Les applications console, GUI et de service sont prises en charge. Le système fournit une interopérabilité à travers la limite 32/64 pour des scénarios tels que couper et coller et COM. Toutefois, les processus 32 bits ne peuvent pas charger les dll 64 bits pour l’exécution, et les processus 64 bits ne peuvent pas charger les dll 32 bits pour l’exécution. Cette restriction ne s’applique pas aux DLL chargées en tant que fichiers de données ou fichiers de ressources d’image. Pour plus d’informations, consultez [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Une application 32 bits peut détecter si elle s’exécute sous WOW64 en appelant la fonction [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (utilisez [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) si vous ciblez Windows 10). L’application peut obtenir des informations supplémentaires sur le processeur à l’aide de la fonction [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Notez que Windows 64 bits ne prend pas en charge l’exécution d’applications Windows 16 bits. La raison principale est que les handles ont 32 bits significatifs sur Windows 64 bits. Par conséquent, les handles ne peuvent pas être tronqués et passés à des applications 16 bits sans perte de données. Les tentatives de lancement d’applications 16 bits échouent avec l’erreur suivante : **erreur \_ \_ \_ format exe incorrect**.

## <a name="in-this-section"></a>Dans cette section

-   [Performances et consommation de mémoire sous WOW64](performance-and-memory-consumption.md)
-   [Détails de l’implémentation WOW64](wow64-implementation-details.md)
-   [Redirecteur du Registre](registry-redirector.md)
-   [Redirecteur de système de fichiers](file-system-redirector.md)
-   [Gestion de la mémoire](memory-management.md)
-   [Affinité du processeur](processor-affinity.md)
-   [Communication entre processus](interprocess-communication.md)
-   [Installation de l’application](application-installation.md)
-   [Débogage de WOW64](debugging-wow64.md)

 

 