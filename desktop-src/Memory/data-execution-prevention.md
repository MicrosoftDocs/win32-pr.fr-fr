---
description: la prévention de l’exécution des données (DEP) est une fonctionnalité de protection de la mémoire au niveau du système qui est intégrée au système d’exploitation à partir de Windows XP et Windows Server 2003.
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: Prévention de l’exécution des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094177"
---
# <a name="data-execution-prevention"></a>Prévention de l’exécution des données

la prévention de l’exécution des données (DEP) est une fonctionnalité de protection de la mémoire au niveau du système qui est intégrée au système d’exploitation à partir de Windows XP et Windows Server 2003. DEP permet au système de marquer une ou plusieurs pages de mémoire comme non exécutables. Le marquage de régions de mémoire comme non exécutables signifie que le code ne peut pas être exécuté à partir de cette région de mémoire, ce qui complique l’exploitation des dépassements de mémoire tampon.

DEP empêche l’exécution de code à partir de pages de données telles que le tas par défaut, les piles et les pools de mémoire. Si une application tente d’exécuter du code à partir d’une page de données protégée, une exception de violation d’accès à la mémoire se produit et, si l’exception n’est pas gérée, le processus appelant se termine.

DEP n’est pas conçu pour être une protection complète contre toutes les attaques. Il s’agit d’un autre outil que vous pouvez utiliser pour sécuriser votre application.

## <a name="how-data-execution-prevention-works"></a>Fonctionnement de la prévention de l’exécution des données

Si une application tente d’exécuter du code à partir d’une page protégée, l’application reçoit une exception avec **la \_ \_ violation d’accès État** du code d’État. Si votre application doit exécuter du code à partir d’une page de mémoire, elle doit allouer et définir les attributs de protection de la [mémoire](memory-protection.md) virtuelle appropriés. La mémoire allouée doit être marquée **page \_ Execute**, **page \_ Execute \_ Read**, **page \_ Execute \_ ReadWrite** ou **page \_ Execute \_ WRITECOPY** lors de l’allocation de mémoire. Les allocations de tas effectuées en appelant les fonctions **malloc** et [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) ne sont pas exécutables.

Les applications ne peuvent pas exécuter le code à partir du tas de processus par défaut ou de la pile.

DEP est configuré au démarrage du système en fonction du paramètre de stratégie de protection des pages non exécutées dans les données de configuration de démarrage. Une application peut récupérer le paramètre de stratégie actuel en appelant la fonction [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) . Selon le paramètre de stratégie, une application peut modifier le paramètre DEP du processus en cours en appelant la fonction [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) .

## <a name="programming-considerations"></a>Éléments de programmation à prendre en considération

Une application peut utiliser la fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) pour allouer de la mémoire exécutable avec les options de protection de la mémoire appropriées. Il est suggéré qu’une application ait défini au minimum l’option de protection **page \_ Execute** Memory. Une fois le code exécutable généré, il est recommandé que l’application définisse des protections de mémoire pour interdire l’accès en écriture à la mémoire allouée. Les applications peuvent interdire l’accès en écriture à la mémoire allouée à l’aide de la fonction [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) . Interdire l’accès en écriture garantit une protection maximale pour les régions exécutables de l’espace d’adressage de processus. Vous devez essayer de créer des applications qui utilisent le plus petit espace d’adressage exécutable possible, ce qui réduit la quantité de mémoire exposée à l’exploitation de la mémoire.

Vous devez également essayer de contrôler la disposition de la mémoire virtuelle de votre application et de créer des régions exécutables. Ces régions exécutables doivent se trouver dans un espace mémoire inférieur à celui des régions non exécutables. En localisant les régions exécutables sous des régions non exécutables, vous pouvez empêcher un dépassement de capacité de la mémoire tampon de déborder dans la zone exécutable de la mémoire.

## <a name="application-compatibility"></a>Compatibilité des applications

Certaines fonctionnalités de l’application sont incompatibles avec DEP. Les applications qui effectuent la génération de code dynamique (par exemple, la génération de code juste-à-temps) et ne marquent pas explicitement le code généré avec l’autorisation EXECUTE peuvent avoir des problèmes de compatibilité sur les ordinateurs qui utilisent DEP. Les applications écrites dans le Active Template Library (ATL) version 7,1 et les versions antérieures peuvent tenter d’exécuter du code sur des pages marquées comme non exécutables, ce qui déclenche une erreur NX et met fin à l’application. Pour plus d’informations, consultez [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy). La plupart des applications qui effectuent des actions incompatibles avec DEP doivent être mises à jour pour fonctionner correctement.

Un petit nombre de fichiers exécutables et de bibliothèques peuvent contenir du code exécutable dans la section des données d’un fichier image. Dans certains cas, les applications peuvent placer de petits segments de code (communément appelés thunks) dans les sections de données. Toutefois, DEP marque les sections du fichier image chargées en mémoire comme étant non exécutables, sauf si l’attribut Executable est appliqué à la section.

Par conséquent, le code exécutable dans les sections de données doit être migré vers une section de code, ou la section de données qui contient le code exécutable doit être explicitement marquée comme exécutable. L’attribut exécutable, l' **image \_ SCN \_ MEM \_ Execute**, doit être ajouté au champ **caractéristiques** de l’en-tête de la section correspondante pour les sections qui contiennent du code exécutable. Pour plus d’informations sur l’ajout d’attributs à une section, consultez la documentation fournie avec votre éditeur de liens.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prévention de l’exécution des données (TechNet)](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[Comment configurer la protection de la mémoire](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[Article 875352 de la base de connaissances](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
