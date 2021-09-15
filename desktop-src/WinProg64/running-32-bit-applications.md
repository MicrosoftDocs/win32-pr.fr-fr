---
title: Exécution d’applications 32 bits
description: exécutez des applications basées sur le Windows 32 bits en toute transparence sur 64 bits Windows avec l’émulateur WOW64 x86. En savoir plus sur le directeur du Registre, le redirecteur du système de fichiers, l’installation des applications sur les systèmes 64 bits et le débogage de WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- programmation Windows WOW64 64 bits
- WOW64 64-bit Windows programmation, à propos de
- applications 32 bits sur 64 bits Windows 64 bits Windows programmation
- 64-bit Windows guide de programmation 64 bits Windows programmation, wow64 voir wow64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127532160"
---
# <a name="running-32-bit-applications"></a>Exécution d’applications 32 bits

WOW64 est l’émulateur x86 qui permet aux applications basées sur Windows 32 bits de s’exécuter de façon transparente sur les Windows 64 bits. cela permet aux applications de Windows de 32 bits (x86) de s’exécuter en toute transparence dans les Windows 64 bits (x64), ainsi que pour 32 les applications Windows 32 bits (x86) et-bit (ARM) pour s’exécuter en toute transparence dans le Windows 64 bits (ARM64). WOW64 est fourni avec le système d’exploitation et n’a pas besoin d’être explicitement activé. Pour plus d’informations, consultez détails de l' [implémentation WOW64](wow64-implementation-details.md).

Le système isole les applications 32 bits des applications 64 bits, ce qui comprend la prévention des collisions de fichiers et de registres. Les applications console, GUI et de service sont prises en charge. Le système fournit une interopérabilité à travers la limite 32/64 pour des scénarios tels que couper et coller et COM. Toutefois, les processus 32 bits ne peuvent pas charger les dll 64 bits pour l’exécution, et les processus 64 bits ne peuvent pas charger les dll 32 bits pour l’exécution. Cette restriction ne s’applique pas aux DLL chargées en tant que fichiers de données ou fichiers de ressources d’image. Pour plus d’informations, consultez [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Une application 32 bits peut détecter si elle s’exécute sous WOW64 en appelant la fonction [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (utilisez [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) si vous ciblez Windows 10). L’application peut obtenir des informations supplémentaires sur le processeur à l’aide de la fonction [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

notez que le Windows 64 bits ne prend pas en charge l’exécution d’applications basées sur Windows 16 bits. La raison principale est que les handles ont 32 bits significatifs sur le Windows 64 bits. Par conséquent, les handles ne peuvent pas être tronqués et passés à des applications 16 bits sans perte de données. Les tentatives de lancement d’applications 16 bits échouent avec l’erreur suivante : **erreur \_ \_ \_ format exe incorrect**.

## <a name="in-this-section"></a>Dans cette section

-   [Performances et consommation de mémoire sous WOW64](performance-and-memory-consumption.md)
-   [Détails de l’implémentation WOW64](wow64-implementation-details.md)
-   [Redirecteur du Registre](registry-redirector.md)
-   [Redirecteur de système de fichiers](file-system-redirector.md)
-   [Gestion de la mémoire](memory-management.md)
-   [Affinité du processeur](processor-affinity.md)
-   [Communication entre processus](interprocess-communication.md)
-   [Installation d’application](application-installation.md)
-   [Débogage de WOW64](debugging-wow64.md)

 

 