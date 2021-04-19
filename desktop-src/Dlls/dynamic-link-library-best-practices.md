---
description: La création de dll présente un certain nombre de défis pour les développeurs.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Meilleures pratiques pour la bibliothèque Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88aba0999f3d0825c6d2f4df3afe09d766a82232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540902"
---
# <a name="dynamic-link-library-best-practices"></a>Meilleures pratiques pour la bibliothèque Dynamic-Link

* * Mis à jour : * *

-   17 mai, 2006

**API importantes**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

La création de dll présente un certain nombre de défis pour les développeurs. Les dll n’ont pas de contrôle de version appliqué par le système. Lorsque plusieurs versions d’une DLL existent sur un système, la facilité de remplacement couplée à l’absence d’un schéma de contrôle de version crée des conflits d’API et de dépendances. La complexité de l’environnement de développement, l’implémentation du chargeur et les dépendances de DLL ont créé des fragilité dans l’ordre de chargement et le comportement de l’application. Enfin, de nombreuses applications reposent sur des dll et des ensembles complexes de dépendances qui doivent être respectées pour que les applications fonctionnent correctement. Ce document fournit des instructions pour les développeurs de DLL pour vous aider à créer des dll plus robustes, portables et extensibles.

Une synchronisation incorrecte dans [**DllMain**](dllmain.md) peut provoquer le blocage d’une application ou l’accès à des données ou du code dans une DLL non initialisée. L’appel de certaines fonctions à partir de **DllMain** provoque de tels problèmes.

![que se passe-t-il quand une bibliothèque est chargée ?](images/fig1.png)

## <a name="general-best-practices"></a>Bonnes pratiques générales

[**DllMain**](dllmain.md) est appelé alors que le verrouillage du chargeur est maintenu. Par conséquent, des restrictions significatives sont imposées sur les fonctions qui peuvent être appelées dans **DllMain**. Par conséquent, **DllMain** est conçu pour effectuer des tâches d’initialisation minimales, à l’aide d’un petit sous-ensemble de l’API Microsoft® Windows®. Vous ne pouvez pas appeler une fonction dans **DllMain** qui tente directement ou indirectement d’acquérir le verrou du chargeur. Dans le cas contraire, vous présenterez la possibilité que votre application se bloque ou tombe en panne. Une erreur dans une implémentation de **DllMain** peut compromettre l’ensemble du processus et de tous ses threads.

La [**DllMain**](dllmain.md) idéale serait simplement un stub vide. Toutefois, étant donné la complexité de nombreuses applications, cela est généralement trop restrictif. Une bonne règle empirique pour **DllMain** consiste à différer le plus possible de l’initialisation. L’initialisation tardive augmente la robustesse de l’application, car cette initialisation n’est pas effectuée tant que le verrouillage du chargeur est maintenu. En outre, l’initialisation tardive vous permet d’utiliser en toute sécurité une plus grande partie de l’API Windows.

Certaines tâches d’initialisation ne peuvent pas être reportées. Par exemple, une DLL qui dépend d’un fichier de configuration ne peut pas se charger si le fichier est incorrect ou contient des opérations garbage. Pour ce type d’initialisation, la DLL doit essayer l’action et échouer rapidement plutôt que gaspiller des ressources en effectuant d’autres tâches.

Vous ne devez jamais effectuer les tâches suivantes à partir de [**DllMain**](dllmain.md):

-   Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (directement ou indirectement). Cela peut provoquer un blocage ou un incident.
-   Appelez [**GetStringTypeA**](/windows/desktop/api/winnls/nf-winnls-getstringtypea), [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)ou [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (directement ou indirectement). Cela peut provoquer un blocage ou un incident.
-   Synchroniser avec d’autres threads. Cela peut provoquer un blocage.
-   Obtenez un objet de synchronisation détenu par du code qui attend pour acquérir le verrou du chargeur. Cela peut provoquer un blocage.
-   Initialisez les threads COM à l’aide de [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Dans certaines conditions, cette fonction peut appeler [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa).
-   Appelez les fonctions du Registre. Ces fonctions sont implémentées dans Advapi32.dll. Si Advapi32.dll n’est pas initialisé avant votre DLL, la DLL peut accéder à la mémoire non initialisée et provoquer le blocage du processus.
-   Appelez [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa). La création d’un processus peut charger une autre DLL.
-   Appelez [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). La sortie d’un thread pendant le détachement de la DLL peut entraîner une nouvelle acquisition du verrou du chargeur, provoquant un blocage ou un incident.
-   Appelez [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread). La création d’un thread peut fonctionner si vous n’effectuez pas de synchronisation avec d’autres threads, mais cela est risqué.
-   Créez un canal nommé ou un autre objet nommé (Windows 2000 uniquement). Dans Windows 2000, les objets nommés sont fournis par la DLL des services Terminal Server. Si cette DLL n’est pas initialisée, les appels à la DLL peuvent entraîner le blocage du processus.
-   Utilisez la fonction de gestion de la mémoire du Run-Time dynamique C (CRT). Si la DLL CRT n’est pas initialisée, les appels à ces fonctions peuvent provoquer le blocage du processus.
-   Appeler des fonctions dans User32.dll ou Gdi32.dll. Certaines fonctions chargent une autre DLL, qui ne peut pas être initialisée.
-   Utilisez du code managé.

Les tâches suivantes peuvent être effectuées en toute sécurité dans **DllMain**:

-   Initialiser des structures de données et des membres statiques au moment de la compilation.
-   Créer et initialiser des objets de synchronisation.
-   Allouez de la mémoire et initialisez les structures de données dynamiques (en évitant les fonctions mentionnées ci-dessus).
-   Configurez le stockage local des threads (TLS).
-   Ouvrir, lire et écrire dans des fichiers.
-   Appeler des fonctions dans Kernel32.dll (à l’exception des fonctions répertoriées ci-dessus).
-   Affectez la valeur NULL aux pointeurs globaux, en déplaçant l’initialisation des membres dynamiques. Dans Microsoft Windows Vista™, vous pouvez utiliser les fonctions d’initialisation unique pour garantir qu’un bloc de code n’est exécuté qu’une seule fois dans un environnement multithread.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Interblocages dus à une inversion d’ordre de verrouillage

Lorsque vous implémentez du code qui utilise plusieurs objets de synchronisation tels que des verrous, il est essentiel d’respecter l’ordre de verrouillage. Lorsqu’il est nécessaire d’acquérir plusieurs verrous à la fois, vous devez définir une priorité explicite appelée hiérarchie de verrouillage ou ordre de verrouillage. Par exemple, si le verrou A est acquis avant le verrou B quelque part dans le code, et que le verrou B est acquis avant le verrou C ailleurs dans le code, l’ordre de verrouillage est A, B, C et cet ordre doit être suivi dans l’ensemble du code. L’inversion d’ordre de verrouillage se produit lorsque l’ordre de verrouillage n’est pas suivi, par exemple, si le verrou B est acquis avant le verrouillage A. l’inversion d’ordre de verrou peut provoquer des blocages difficiles à déboguer. Pour éviter de tels problèmes, tous les threads doivent acquérir des verrous dans le même ordre.

Il est important de noter que le chargeur appelle [**DllMain**](dllmain.md) avec le verrou du chargeur déjà acquis, de sorte que le verrouillage du chargeur doit avoir la priorité la plus élevée dans la hiérarchie de verrouillage. Notez également que le code doit acquérir les verrous requis pour une synchronisation correcte ; Il n’est pas nécessaire d’acquérir chaque verrou unique défini dans la hiérarchie. Par exemple, si une section de code requiert uniquement les verrous A et C pour une synchronisation correcte, le code doit acquérir le verrou A avant d’acquérir le verrou C ; Il n’est pas nécessaire que le code acquière également le verrou B. En outre, le code DLL ne peut pas acquérir explicitement le verrou du chargeur. Si le code doit appeler une API telle que [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) qui peut acquérir indirectement le verrou du chargeur et que le code doit également acquérir un verrou privé, le code doit appeler **GetModuleFileName** avant d’acquérir le verrou P, garantissant ainsi que l’ordre de chargement est respecté.

La figure 2 est un exemple qui illustre l’inversion de l’ordre de verrouillage. Prenons l’exemple d’une DLL dont le thread principal contient [**DllMain**](dllmain.md). Le chargeur de bibliothèque acquiert le verrou de chargeur L, puis appelle **DllMain**. Le thread principal crée les objets de synchronisation A, B et G pour sérialiser l’accès à ses structures de données, puis tente d’acquérir le verrou G. Un thread de travail qui a déjà acquis le verrou G appelle ensuite une fonction telle que GetModuleHandle qui tente d’acquérir le verrou de chargeur L. Ainsi, le thread de travail est bloqué sur L et le thread principal est bloqué sur G, provoquant ainsi un blocage.

![interblocage provoqué par une inversion d’ordre de verrouillage](images/fig2.png)

Pour empêcher les blocages causés par l’inversion d’ordre de verrouillage, tous les threads doivent tenter d’acquérir des objets de synchronisation dans l’ordre de chargement défini à tout moment.

## <a name="best-practices-for-synchronization"></a>Meilleures pratiques pour la synchronisation

Prenons l’exemple d’une DLL qui crée des threads de travail dans le cadre de son initialisation. Lors du nettoyage des DLL, il est nécessaire de synchroniser avec tous les threads de travail pour vérifier que les structures de données sont dans un état cohérent, puis mettre fin aux threads de travail. Aujourd’hui, il n’existe aucun moyen simple de résoudre complètement le problème de synchronisation et d’arrêt corrects des dll dans un environnement multithread. Cette section décrit les meilleures pratiques actuelles pour la synchronisation des threads lors de l’arrêt de la DLL.

Synchronisation des threads dans [**DllMain**](dllmain.md) pendant la sortie du processus

-   Au moment où [**DllMain**](dllmain.md) est appelé à la sortie du processus, tous les threads du processus ont été nettoyés de force et il y a un risque que l’espace d’adressage soit incohérent. La synchronisation n’est pas requise dans ce cas. En d’autres termes, le \_ Gestionnaire de détachement de processus de dll idéal \_ est vide.
-   Windows Vista garantit que les structures de données principales (variables d’environnement, répertoire actif, tas de processus, etc.) sont dans un état cohérent. Toutefois, d’autres structures de données peuvent être endommagées, de sorte que le nettoyage de la mémoire n’est pas sécurisé.
-   L’état persistant qui doit être enregistré doit être vidé dans un stockage permanent.

Synchronisation de threads dans **DllMain** pour le \_ \_ détachement de thread dll pendant le DÉchargement de dll

-   Lorsque la DLL est déchargée, l’espace d’adressage n’est pas rejeté. Par conséquent, la DLL est supposée effectuer un arrêt propre. Cela comprend la synchronisation des threads, les handles ouverts, l’état persistant et les ressources allouées.
-   La synchronisation des threads est délicate car l’attente de la fermeture des threads dans [**DllMain**](dllmain.md) peut provoquer un blocage. Par exemple, la DLL A contient le verrou du chargeur. Il signale le thread T pour quitter et attend que le thread se termine. Le thread T se termine et le chargeur tente d’acquérir le verrou du chargeur pour appeler le **DllMain** de la dll A avec le \_ \_ détachement de thread dll. Cela provoque un interblocage. Pour réduire le risque d’un blocage :
    -   DLL A obtient un \_ message de \_ détachement de thread dll dans son [**DllMain**](dllmain.md) et définit un événement pour le thread T, en lui signalant de quitter.
    -   Le thread T termine sa tâche actuelle, se met à un état cohérent, signale la DLL A et attend une attente infinie. Notez que les routines de vérification de cohérence doivent respecter les mêmes restrictions que [**DllMain**](dllmain.md) pour éviter les interblocages.
    -   La DLL A termine T, sachant qu’elle est dans un état cohérent.

Si une DLL est déchargée une fois que tous ses threads ont été créés, mais avant qu’ils ne commencent à s’exécuter, les threads peuvent se bloquer. Si la DLL crée des threads dans son **DllMain** dans le cadre de son initialisation, certains threads n’ont peut-être pas terminé l’initialisation et le \_ message d’attachement de thread dll \_ est toujours en attente de remise à la dll. Dans ce cas, si la DLL est déchargée, elle commence à mettre fin aux threads. Toutefois, certains threads peuvent être bloqués derrière le verrou du chargeur. Leurs \_ \_ messages d’attachement de thread dll sont traités après que la dll a été démappée, provoquant ainsi le blocage du processus.

## <a name="recommendations"></a>Recommandations

Les recommandations suivantes sont recommandées :

-   Utilisez Application Verifier pour intercepter les erreurs les plus courantes dans [**DllMain**](dllmain.md).
-   Si vous utilisez un verrou privé à l’intérieur de [**DllMain**](dllmain.md), définissez une hiérarchie de verrouillage et utilisez-la de manière cohérente. Le verrouillage du chargeur doit être en bas de cette hiérarchie.
-   Vérifiez qu’aucun appel ne dépend d’une autre DLL qui n’a peut-être pas encore été entièrement chargée.
-   Effectuez des initialisations simples statiques au moment de la compilation, plutôt que dans [**DllMain**](dllmain.md).
-   Différer tous les appels dans [**DllMain**](dllmain.md) qui peuvent attendre jusqu’à une date ultérieure.
-   Différer les tâches d’initialisation qui peuvent attendre jusqu’à une date ultérieure. Certaines conditions d’erreur doivent être détectées tôt pour que l’application puisse gérer les erreurs correctement. Toutefois, il existe des compromis entre cette détection précoce et la perte de robustesse qui peut en résulter. Le report de l’initialisation est souvent préférable.

 

 
