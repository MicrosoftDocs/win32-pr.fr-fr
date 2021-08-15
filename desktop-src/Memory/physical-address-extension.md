---
description: L’extension d’adresse physique (PAE) est une fonctionnalité de processeur qui permet aux processeurs x86 d’accéder à plus de 4 Go de mémoire physique sur les versions de Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Extension d’adresse physique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2fd9193a19d228f26a09865086c59b65c0019b3cee42142dfd27188eff30169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979719"
---
# <a name="physical-address-extension"></a>Extension d’adresse physique

L’extension d’adresse physique (PAE) est une fonctionnalité de processeur qui permet aux processeurs x86 d’accéder à plus de 4 Go de mémoire physique sur les versions de Windows. certaines versions 32 bits de Windows Server s’exécutant sur des systèmes x86 peuvent utiliser PAE pour accéder jusqu’à 64 go ou 128 go de mémoire physique, en fonction de la taille d’adresse physique du processeur. pour plus d’informations, consultez [limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md).

Les architectures de processeur Intel Itanium et x64 peuvent accéder à plus de 4 Go de mémoire physique en mode natif et, par conséquent, ne fournissent pas l’équivalent d’PAE. PAE est utilisé uniquement par les versions 32 bits de Windows s’exécutant sur des systèmes x86.

Avec PAE, le système d’exploitation passe de la traduction d’adresses linéaires à deux niveaux à la traduction d’adresses à trois niveaux. Au lieu d’une adresse linéaire qui est divisée en trois champs distincts pour l’indexation dans des tables de mémoire, elle est divisée en quatre champs distincts : un champ de bits de 2 bits, de 2 9 bits et un champ de bits de 12 bits qui correspond à la taille de page implémentée par l’architecture Intel (4 Ko). La taille des entrées de table de pages (PTE) et des entrées de répertoire de page (PDEs) en mode PAE est augmentée de 32 à 64 bits. Les bits supplémentaires permettent à une PTE ou PDE de système d’exploitation de référencer la mémoire physique au-delà de 4 Go.

dans les Windows 32 bits s’exécutant sur des systèmes x64, PAE offre également plusieurs fonctionnalités avancées du système et du processeur, notamment la [prévention de l’exécution des données](data-execution-prevention.md) (DEP), l’accès à la [mémoire non uniforme (NUMA)](../procthread/numa-support.md)et la possibilité d’ajouter de la mémoire à un système pendant qu’il est en cours d’exécution (ajout de mémoire à chaud).

PAE ne modifie pas la quantité d’espace d’adressage virtuel disponible pour un processus. chaque processus s’exécutant en Windows de 32 bits est toujours limité à un espace d’adressage virtuel de 4 go.

## <a name="system-support-for-pae"></a>Prise en charge du système PAE

PAE est pris en charge uniquement sur les versions 32 bits suivantes de Windows s’exécutant sur des systèmes x86 :

-   Windows 7 (32 bits uniquement)
-   Windows Serveur 2008 (32 bits uniquement)
-   Windows Vista (32 bits uniquement)
-   Windows Serveur 2003 (32 bits uniquement)
-   Windows XP (32 bits uniquement)

## <a name="enabling-pae"></a>Activation d’PAE

Windows active automatiquement PAE si dep est activé sur un ordinateur qui prend en charge la prévention de l’exécution de la configuration matérielle, ou si l’ordinateur est configuré pour l’ajout à chaud de périphériques mémoire dans des plages de mémoire au-delà de 4 go. Si l’ordinateur ne prend pas en charge la DEP avec matériel ou n’est pas configuré pour les périphériques d’ajout de mémoire à chaud dans des plages de mémoire au-delà de 4 Go, PAE doit être explicitement activé.

Pour activer explicitement PAE, utilisez la commande [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) suivante pour définir l’option d’entrée de démarrage **PAE** :

 **bcdedit/set \[ {ID} \] PAE ForceEnable**  


Si la DEP est activée, les PAE ne peuvent pas être désactivées. Utilisez les commandes de commande [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) suivantes pour désactiver DEP et PAE :

 **bcdedit/set \[ {ID} \] NX AlwaysOff**  
**bcdedit/set \[ {ID} \] PAE ForceDisable**  


**Windows Server 2003 et Windows XP :** Pour activer PAE, utilisez le commutateur **/PAE** dans le fichier [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) . Pour désactiver PAE, utilisez le commutateur **/NOPAE** . Pour désactiver DEP, utilisez le commutateur **/Execute** .

## <a name="comparing-pae-and-other-large-memory-support"></a>Comparaison de la prise en charge d’PAE et d’autres mémoires volumineuses

PAE, [réglage à 4 gigaoctets](4-gigabyte-tuning.md) (4GT) et AWE ( [Address Windowing Extensions](address-windowing-extensions.md) ) offrent des finalités différentes et peuvent être utilisés indépendamment les uns des autres :

-   PAE permet au système d’exploitation d’accéder à plus de 4 Go de mémoire physique et de l’utiliser.
-   4GT augmente la partie de l’espace d’adressage virtuel disponible pour un processus de 2 Go jusqu’à 3 Go.
-   AWE est un ensemble d’API qui permet à un processus d’allouer de la mémoire physique non paginée, puis de mapper dynamiquement des parties de cette mémoire dans l’espace d’adressage virtuel du processus.

Si les options 4GT et AWE ne sont pas utilisées, la quantité de mémoire physique qu’un seul processus 32 bits peut utiliser est limitée par la taille de son espace d’adressage (2 Go). Dans ce cas, un système compatible PAE peut toujours utiliser plus de 4 Go de RAM pour exécuter plusieurs processus en même temps ou pour mettre en cache les données de fichier en mémoire.

4GT peut être utilisé avec ou sans PAE. toutefois, certaines versions de Windows limitent la quantité maximale de mémoire physique qui peut être prise en charge lors de l’utilisation de 4gt. Sur ces systèmes, le démarrage avec 4GT activé force le système d’exploitation à ignorer toute mémoire dépassant la limite.

AWE ne requiert pas PAE ou 4GT, mais il est souvent utilisé avec PAE pour allouer plus de 4 Go de mémoire physique à partir d’un seul processus 32 bits.

## <a name="related-topics"></a>Rubriques connexes



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Informations techniques de référence sur PAE x86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
