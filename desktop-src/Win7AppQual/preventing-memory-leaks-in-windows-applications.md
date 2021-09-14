---
description: découvrez comment empêcher les fuites de mémoire dans les applications Windows pour les plateformes Windows 7 et Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: prévention des fuites de mémoire dans les Applications Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414548"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>prévention des fuites de mémoire dans les Applications Windows

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  

## <a name="description"></a>Description

Les fuites de mémoire sont une classe de bogues dans laquelle l’application ne parvient pas à libérer de la mémoire lorsqu’elle n’est plus nécessaire. Au fil du temps, les fuites de mémoire affectent les performances de l’application en question, ainsi que du système d’exploitation. Une fuite importante peut entraîner des temps de réponse inacceptable en raison d’une pagination excessive. Finalement, l’application, ainsi que d’autres parties du système d’exploitation, rencontrent des défaillances.

Windows libérera toute la mémoire allouée par l’application lors de l’arrêt du processus, si bien que les applications à exécution réduite n’affecteront pas de manière significative les performances globales du système. toutefois, les fuites dans les processus de longue durée, telles que les services ou les plug-ins d’explorateur peuvent avoir un impact considérable sur la fiabilité du système et peuvent obliger l’utilisateur à redémarrer Windows afin de rendre le système utilisable à nouveau.

Les applications peuvent allouer de la mémoire en leur nom par plusieurs moyens. Chaque type d’allocation peut entraîner une fuite si elle n’est pas libérée après utilisation. Voici quelques exemples de modèles d’allocation courants :

-   Mémoire du tas via la fonction [**HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) ou ses équivalents de Runtime C/C++ **malloc** ou **New**
-   Allocation directe à partir du système d’exploitation via la fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .
-   Les handles de noyau créés via des API Kernel32 telles que [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea), [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)ou [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)détiennent la mémoire du noyau pour le compte de l’application.
-   Les handles GDI et utilisateur créés via les API User32 et gdi32 (par défaut, chaque processus a un quota de 10 000 descripteurs)

## <a name="best-practices"></a>Bonnes pratiques

La surveillance de la consommation des ressources de votre application au fil du temps est la première étape de la détection et du diagnostic des fuites de mémoire. utilisez Windows gestionnaire des tâches et ajoutez les colonnes suivantes : « taille de validation », « handles », « objets utilisateur » et « objets GDI ». Cela vous permettra d’établir une ligne de base pour votre application et de surveiller l’utilisation des ressources au fil du temps.

![capture d’écran montrant la page « processus » dans Windows gestionnaire des tâches.](images/preventingmemoryleaks-windowstaskmanager.gif)

Les outils Microsoft suivants fournissent des informations plus détaillées et peuvent aider à détecter et à diagnostiquer les fuites pour les différents types d’allocation dans votre application :

-   l’analyseur de performances et les moniteur de ressource font partie de Windows 7 et peuvent surveiller et tracer l’utilisation des ressources au fil du temps
-   la dernière version de Application Verifier peut diagnostiquer les fuites de tas sur Windows 7
-   UMDH, qui fait partie des outils de débogage pour Windows, analyse les allocations de mémoire du tas pour un processus donné et peut aider à trouver des fuites et d’autres modèles d’utilisation inhabituels.
-   Xperf est un outil d’analyse des performances sophistiqué avec prise en charge des traces d’allocation de tas
-   Le tas de débogage CRT effectue le suivi des allocations de tas et peut vous aider à générer vos propres fonctionnalités de débogage de tas

Certaines pratiques de codage et de conception peuvent limiter le nombre de fuites dans votre code.

-   Utilisez des pointeurs intelligents dans du code C++ pour les allocations de tas, ainsi que pour les ressources Win32, telles que les **Handles** de noyau. La bibliothèque C++ standard fournit la **classe \_ ptr automatique** pour les allocations de tas. Pour les autres types d’allocation, vous devez écrire vos propres classes. La bibliothèque ATL fournit un ensemble complet de classes pour la gestion automatique des ressources pour les objets de segment de mémoire et les handles de noyau
-   Utilisez des fonctionnalités intrinsèques du compilateur comme **\_ com \_ ptr \_ t** pour encapsuler vos pointeurs d’interface com en « pointeurs intelligents » et pour faciliter le décompte de références. Il existe des classes similaires pour les autres types de données COM : **\_ BSTR \_ t** et **\_ Variant \_ t**
-   Surveillez l’utilisation inhabituelle de la mémoire dans le code .NET. Le code managé n’est pas immunisé contre les fuites de mémoire. Consultez [« suivi des fuites de mémoire managées »](/archive/blogs/ricom/) pour savoir comment rechercher des fuites de gc
-   Tenez compte des modèles de fuite dans le code côté client Web. les références circulaires entre les objets COM et les moteurs de script comme JScript peuvent provoquer des fuites importantes dans les applications web. [« Comprendre et résoudre les modèles de fuites d’Internet Explorer »](/previous-versions/ms976398(v=msdn.10)) contient plus d’informations sur ces types de fuites. Vous pouvez utiliser le détecteur de fuites de mémoire JavaScript pour déboguer les fuites de mémoire dans votre code. si Windows Internet Explorer 8, qui est livré avec Windows 7, atténue la plupart de ces problèmes, les navigateurs plus anciens restent vulnérables à ces bogues.
-   Évitez d’utiliser plusieurs chemins de sortie à partir d’une fonction. Les allocations affectées aux variables à la portée de la fonction doivent être libérées dans un bloc particulier à la fin de la fonction
-   N’utilisez pas d’exceptions dans votre code sans libérer toutes les variables locales dans les fonctions. Si vous utilisez des exceptions natives, libérez toutes vos allocations dans le \_ \_ bloc finally. Si vous utilisez des exceptions C++, vous devez encapsuler tous vos tas et les allocations de handle dans des pointeurs intelligents
-   Ne pas supprimer ou réinitialiser un objet [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sans appeler la fonction [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Liens vers les ressources

*Modèles d’allocation courants :*

-   [**Fonction d’allocation du tas**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Fonction d’allocation de mémoire**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**New, opérateur (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Fonction d’allocation virtuelle**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Objets de noyau](../sysinfo/kernel-objects.md)
-   [Handles d’objet GDI](../sysinfo/gdi-objects.md)
-   [Handles d’objet d’interface utilisateur](../sysinfo/user-objects.md)

*Outils Microsoft :*

-   [Application Verifier](application-verifier.md)
-   [Outils de débogage pour Windows](/windows-hardware/drivers/debugger/)
-   [Segment de mémoire de vidage en mode utilisateur](/windows-hardware/drivers/debugger/umdh)
-   [Outil de capture, de traitement et d’analyse de trace](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [Tas de débogage CRT](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Liens supplémentaires :*

-   [**\_classe PTR automatique**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Classes de mémoire Active Template Library (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_\_objet com PTR \_ t**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_BSTR \_ t (classe)**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_\_classe YT variant**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   [« Suivi des fuites de mémoire gérées »](/archive/blogs/ricom/)
-   [« Comprendre et résoudre les modèles de fuites d’Internet Explorer »](/previous-versions/ms976398(v=msdn.10))
-   [« Détecteur de fuites de mémoire JavaScript »](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Atténuation des fuites de mémoire circulaire (dans les navigateurs) :](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**try-finally, instruction**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**PROPVARIANT, structure**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**PropVariantClear fonction)**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
