---
description: 64 bits uniquement
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: 64 bits uniquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404365"
---
# <a name="64-bit-only"></a>64 bits uniquement

## <a name="affected-platforms"></a>Plateformes affectées

**serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -élevée  






## <a name="description"></a>Description

Windows Le serveur 2008 R2 est fourni avec une référence SKU 64 bits uniquement. aucune référence SKU 32 bits n’est disponible pour la version serveur du système d’exploitation. toutefois, une référence SKU 32 bits continue d’être disponible pour le client Windows 7.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Cela aura un impact sur trois domaines :

-   pilotes 32 bits
-   plug-ins 32 bits
-   exécutables 16 bits

## <a name="solution-for-32-bit-drivers"></a>Solution pour les pilotes 32 bits

Recompilez les pilotes 32 bits comme des pilotes signés 64 bits.

## <a name="solution-for-32-bit-plug-ins"></a>Solution pour les plug-ins 32 bits

WoW64, un émulateur x86, permet aux applications basées sur Windows 32 bits de s’exécuter en toute transparence sur les Windows 64 bits. WoW64 est désormais une fonctionnalité facultative que vous devez installer si nécessaire pour exécuter du code 32 bits.

Le système isole les applications 32 bits des applications 64 bits, ce qui comprend la prévention des collisions de fichiers et de registres. Les applications console, GUI et de service sont prises en charge. Le système fournit une interopérabilité à travers la limite 32/64 pour des scénarios tels que couper et coller et COM. Toutefois, les processus 32 bits ne peuvent pas charger les dll 64 bits et les processus 64 bits ne peuvent pas charger de dll 32 bits. nous le voyons généralement dans les plug-ins de shell écrits pour Windows Explorer.

Une application 32 bits peut détecter si elle s’exécute sous WOW64 en appelant la fonction IsWow64Process. L’application peut obtenir des informations supplémentaires sur le processeur à l’aide de la fonction GetNativeSystemInfo

notez que le Windows 64 bits ne prend pas en charge l’exécution d’applications basées sur Windows 16 bits. La raison principale est que les handles ont 32 bits significatifs sur le Windows 64 bits. Par conséquent, les handles ne peuvent pas être tronqués et passés à des applications 16 bits sans perte de données. Les tentatives de lancement d’applications 16 bits échouent avec l’erreur suivante : erreur \_ \_ format exe incorrect \_ .

## <a name="solution-for-16-bit-executables"></a>Solution pour les exécutables 16 bits

64-bit Windows reconnaît un nombre limité de programmes d’installation 16 bits spécifiques et remplace une version 32 bits. la liste des substitutions est stockée dans le registre sous la clé suivante : HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion NtVdm64 la \\ prise en charge de plusieurs moteurs d’installation est intégrée, y compris les programmes d’installation InstallShield 5. x. notez que l’Windows Installer 64 bits peut installer en toute transparence des applications MSI 32 bits sur des Windows 64 bits.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Exécution d’applications 32 bits](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Performances et consommation de mémoire](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [Détails de l’implémentation WOW64](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Redirecteur du Registre](/windows/desktop/WinProg64/registry-redirector)
-   [Redirecteur de système de fichiers](/windows/desktop/WinProg64/file-system-redirector)
-   [Gestion de la mémoire](/windows/desktop/WinProg64/memory-management)
-   [Affinité du processeur](/windows/desktop/WinProg64/processor-affinity)
-   [Communication entre processus](/windows/desktop/WinProg64/interprocess-communication)
-   [Installation d’applications sur des systèmes 64 bits](/windows/desktop/WinProg64/application-installation)
-   [Débogage de WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**IsWow64Process fonction)**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo fonction)**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
