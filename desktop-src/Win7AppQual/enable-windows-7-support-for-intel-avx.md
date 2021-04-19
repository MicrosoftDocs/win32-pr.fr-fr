---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Activer la prise en charge de Windows 7 pour Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530254"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Activer la prise en charge de Windows 7 pour Intel AVX

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients** -Windows 7 SP1  
**Serveurs** -Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

Intel<sup>?</sup> AVX (Advanced Vector Extensions)<sup>?</sup> est une extension de type vectoriel à virgule flottante 256 bits SIMD de l’architecture Intel. Il comprend des extensions pour les instructions et les ensembles d’registres.

Microsoft a développé des améliorations de l’API, telles que les fonctions XState, qui permettent aux applications d’accéder aux fonctionnalités et à l’état du processeur étendu et de les manipuler, y compris AVX.

## <a name="usage-scenarios"></a>Scénarios d’utilisation

Il existe trois niveaux généraux d’impact potentiel.

**Niveau 1 :** Les applications qui n’utilisent pas directement Intel AVX ne verront aucun impact sur leurs fonctionnalités, même si elles appellent des bibliothèques ou utilisent des compilateurs qui utilisent ou génèrent indirectement des extensions Intel AVX. Cela représente de loin la majorité des applications.

**Niveau 2 :** Les applications avancées qui utilisent explicitement le jeu d’instructions Intel AVX pourront accéder et modifier le contenu du Registre AVX lorsqu’une exception matérielle est générée. Un très petit nombre d’applications se trouve dans cette catégorie, car cela implique une connaissance approfondie du flux d’instructions s’exécutant au moment de l’exception, par exemple les applications avec des sections écrites en langage assembleur ou celles qui génèrent du code machine au moment de l’exécution (par exemple, les runtimes de code managé avec compilation juste-à-temps).

**Niveau 3 :** Les applications du débogueur pourront accéder et manipuler l’État AVX dans l’application en cours de débogage.

## <a name="how-to-leverage-feature-capabilities"></a>Comment tirer parti des fonctionnalités de fonctionnalités

**Niveau 1 :** Aucune action n’est nécessaire pour que les applications utilisent Intel AVX.

**Niveau 2 :** Les applications de cette catégorie peuvent accéder et manipuler l’État AVX au moment de l’exception à partir de leurs filtres d’exception. Après avoir obtenu le contexte du processeur de base via GetExceptionInformation, les filtres doivent :

 **1.** Vérifiez la valeur de l' **indicateur \_ XSTATE du contexte** . Cet indicateur indique la présence d’au moins une fonctionnalité XState dans le contexte.  
**2.** dans ce cas, appelez **GetXStateFeaturesMask** et testez la valeur de l’indicateur **XSTATE \_ AVX** dans le masque retourné. Cela indique la présence de l’État AVX dans le contexte.  
**3.** appelez **LocateXStateFeature** pour récupérer l’emplacement réel où l’État AVX est stocké.  

**Niveau 3 :** Il n’est pas nécessaire de mettre à jour les applications existantes du débogueur, sauf si elles souhaitent accéder aux registres Intel AVX :

**1.** pour déterminer si AVX est activé, le débogueur doit utiliser :

-   GetEnabledXStateFeatures pour obtenir un masque des fonctionnalités XState activées sur les processeurs x86 ou x64 afin de déterminer quelles fonctionnalités sont présentes et activées sur le système avant d’utiliser une fonctionnalité de processeur XState ou de manipuler des contextes XState

  
**2.** si AVX est présent et que vous souhaitez récupérer et manipuler l’État AVX à partir de l’application en cours de débogage (par exemple, GetThreadContext et SetThreadContext), le débogueur doit utiliser :

-   Fonction InitializeContext pour initialiser une structure de contexte à l’intérieur d’une mémoire tampon avec la taille et l’alignement nécessaires
-   Fonction CopyContext pour copier une structure de contexte source (y compris les XState) sur une structure de contexte de destination initialisée

  
**3.** pour tester, définir et localiser l’État AVX dans un contexte de processeur, le débogueur doit utiliser :

-   LocateXStateFeature pour récupérer un pointeur vers l’état du processeur pour une fonctionnalité XState individuelle dans une structure de contexte
-   GetXStateFeaturesMask pour retourner le masque des fonctionnalités XState définies dans une structure de contexte
-   SetXStateFeaturesMask pour définir le masque des fonctionnalités XState définies dans une structure de contexte

  


## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   Pour plus d’informations sur les fonctions XState dans le SDK Windows, consultez [débogage de fonctions](../debug/debugging-functions.md).
-   Pour obtenir une vue d’ensemble des instructions et des fonctionnalités d’Intel AVX, consultez [Intel AVX : nouvelles frontières dans améliorations des performances et efficacité énergétique](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
