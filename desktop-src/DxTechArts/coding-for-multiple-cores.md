---
title: Programmation pour le multicœur sur Xbox 360 et Windows
description: Cette rubrique fournit des conseils sur la prise en main de la programmation multithread.
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7657a5177527f1c13bfb1f0fdd643963a4f670d72b774e4142413231e7e3c58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102365"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>Programmation pour le multicœur sur Xbox 360 et Windows

Pendant des années, les performances des processeurs ont augmenté régulièrement, et les jeux et d’autres programmes ont profité des avantages de cette puissance croissante sans avoir à faire quoi que ce soit.

Les règles ont été modifiées. Les performances des cœurs de processeur unique s’améliorent à présent très lentement, si ce n’est du tout. Toutefois, la puissance de calcul disponible dans un ordinateur ou une console standard continue de croître. La différence réside dans le fait que la majeure partie de ce gain de performances provient désormais de la présence de plusieurs cœurs de processeur sur un seul ordinateur, souvent dans une seule puce. L’UC Xbox 360 possède trois cœurs de processeur sur une seule puce et environ 70% de processeurs PC vendus dans 2006 étaient multicœurs.

Les augmentations de la puissance de traitement disponible sont aussi spectaculaires que dans le passé, mais désormais, les développeurs doivent écrire du code multithread afin d’utiliser cette puissance. La programmation multithread apporte un nouveau défi à la conception et à la programmation. Cette rubrique fournit des conseils sur la prise en main de la programmation multithread.

## <a name="the-importance-of-good-design"></a>L’importance de la bonne conception

Une bonne conception de programme multithread est essentielle, mais elle peut être très difficile. Si vous déplacez par hasard vos principaux systèmes de jeu vers différents threads, vous constaterez probablement que chaque thread consacre la plus grande partie de son temps à attendre les autres threads. Ce type de conception implique une complexité accrue et des efforts de débogage importants, avec pratiquement aucun gain de performances.

Chaque fois que les threads doivent synchroniser ou partager des données, il existe un risque d’altération des données, de surcharge des synchronisations, de blocages et de complexité. Par conséquent, votre conception multithread doit clairement documenter chaque point de synchronisation et de communication, et elle devrait réduire autant que possible ces points. Lorsque les threads ont besoin de communiquer, l’effort de codage augmente, ce qui peut réduire la productivité si elle affecte un code source trop grand.

L’objectif de conception le plus simple pour le multithreading consiste à scinder le code en éléments indépendants de grande taille. Si vous limitez ensuite ces éléments à la communication de quelques fois par trame, vous verrez une accélération significative du multithreading, sans complexité excessive.

## <a name="typical-threaded-tasks"></a>Tâches de thread courantes

Quelques types de tâches ont prouvé qu’elles sont placées sur des threads distincts. La liste suivante n’est pas destinée à être exhaustive, mais elle doit donner quelques idées.

### <a name="rendering"></a>Rendu

Le rendu, qui peut inclure le parcours du graphique de la scène ou, éventuellement, uniquement l’appel de fonctions D3D, est souvent un compte de 50% ou plus du temps processeur. Par conséquent, le déplacement du rendu vers un autre thread peut avoir des avantages significatifs. Le thread de mise à jour peut remplir une sorte de tampon de description de rendu, que le thread de rendu peut ensuite traiter.

Le thread de mise à jour de jeu est toujours une image à l’avance du thread de rendu, ce qui signifie qu’il faut deux frames pour que les actions de l’utilisateur s’affichent à l’écran. Bien que cette latence accrue puisse être un problème, la fréquence d’images accrue du fractionnement de la charge de travail conserve généralement la latence totale acceptable.

Dans la plupart des cas, tout le rendu est toujours effectué sur un thread unique, mais il s’agit d’un thread différent de la mise à jour du jeu.

L' \_ indicateur MULTITHREAD D3DCREATE est parfois utilisé pour autoriser le rendu sur un thread et la création de ressources sur d’autres threads. cet indicateur est ignoré sur la Xbox 360 et vous devez éviter de l’utiliser sur Windows. sur Windows, la spécification de cet indicateur force D3D à consacrer beaucoup de temps à la synchronisation, ce qui ralentit le thread de rendu.

### <a name="file-decompression"></a>Décompression de fichiers

Les temps de chargement sont toujours trop longs et la diffusion en continu des données en mémoire sans affecter la fréquence d’images peut être difficile. Si toutes les données sont compressées de façon agressive sur le disque, la vitesse de transfert des données à partir du disque dur ou du disque optique est moins susceptible d’être un facteur de limitation. Sur un processeur à thread unique, il n’y a généralement pas assez de temps processeur disponible pour la compression afin d’aider à charger les temps. Toutefois, sur un système multiprocesseur, la décompression des fichiers utilise des cycles de processeur qui, sans cela, seraient inutiles. elle améliore le temps de chargement et la diffusion en continu. et économise de l’espace sur le disque.

N’utilisez pas la décompression de fichiers en remplacement du traitement qui doit être effectué pendant la production. Par exemple, si vous dédiez un thread supplémentaire à l’analyse de données XML pendant le chargement de niveau, vous n’utilisez pas le multithreading pour améliorer l’expérience du joueur.

Quand vous utilisez un thread de décompression de fichiers, vous devez toujours utiliser des e/s de fichier asynchrones et des lectures volumineuses afin d’optimiser l’efficacité de la lecture des données.

### <a name="graphics-fluff"></a>Attractifs Graphics

Il existe de nombreux niceties graphiques qui améliorent l’apparence du jeu, mais ne sont pas strictement nécessaires. Il s’agit notamment d’animations Cloud, de simulations de cheveux, d’ondes procédurales, de végétation procédurales, de particules supplémentaires ou d’une physique sans jeu de mesures.

Étant donné que ces effets n’affectent pas le jeu de résultats, ils ne provoquent pas de problèmes de synchronisation difficiles : ils peuvent se synchroniser avec les autres threads une fois par image ou moins souvent. en outre, sur les jeux pour Windows ces effets peuvent ajouter de la valeur pour les joueurs avec des processeurs multicœurs, tout en étant omis en mode silencieux sur les ordinateurs à cœur unique, donnant ainsi un moyen simple de mettre à l’échelle sur un large éventail de fonctionnalités.

### <a name="physics"></a>Physique

La physique ne peut souvent pas être placée sur un thread distinct pour s’exécuter en parallèle avec la mise à jour du jeu, car la mise à jour du jeu requiert généralement les résultats des calculs physiques. L’alternative à la physique du multithreads consiste à l’exécuter sur plusieurs processeurs. Bien que cela puisse être fait, il s’agit d’une tâche complexe nécessitant un accès fréquent aux structures de données partagées. Si vous pouvez maintenir la charge de travail physique suffisamment faible pour tenir sur le thread principal, votre travail sera plus simple.

Les bibliothèques qui prennent en charge l’exécution physique sur plusieurs threads sont disponibles. Toutefois, cela peut entraîner un problème : lorsque votre jeu est en cours d’exécution physique, il utilise de nombreux threads, mais le reste du temps qu’il utilise. L’exécution physique sur plusieurs threads nécessite l’adressage de ce qui permet de répartir uniformément la charge de travail sur le frame. Si vous écrivez un moteur physique multithread, vous devez prêter une attention particulière à toutes vos structures de données, points de synchronisation et équilibrage de charge.

## <a name="example-multithreaded-designs"></a>Exemples de conceptions multithread

les jeux pour Windows doivent s’exécuter sur des ordinateurs avec différents nombres de cœurs de processeur. La plupart des ordinateurs de jeu n’ont toujours qu’un seul cœur, bien que le nombre de machines à deux cœurs augmente rapidement. un jeu typique pour Windows peut endommager sa charge de travail en un seul thread pour la mise à jour et le rendu, avec des threads de travail facultatifs pour l’ajout de fonctionnalités supplémentaires. En outre, certains threads d’arrière-plan pour les e/s de fichier et la mise en réseau seraient probablement utilisés. La figure 1 illustre les threads, ainsi que les principaux points de transfert de données.

**Figure 1. Conception de threads dans un jeu pour Windows**

![conception de threads dans un jeu pour Windows](images/coding-for-multiple-cores-1.gif)

Un jeu Xbox 360 classique peut utiliser des threads logiciels nécessitant beaucoup plus de ressources processeur. il peut donc diviser sa charge de travail en thread de mise à jour, thread de rendu et trois threads de travail, comme illustré à la figure 2.

**Figure 2. Conception de threads dans un jeu pour Xbox 360**

![conception de threads dans un jeu pour Xbox 360](images/coding-for-multiple-cores-2.gif)

À l’exception des e/s de fichier et de la mise en réseau, ces tâches ont toutes le potentiel d’être suffisamment gourmandes en ressources processeur pour tirer parti de leur propre thread matériel. Ces tâches peuvent également être suffisamment indépendantes pour pouvoir s’exécuter pour une trame entière sans communiquer.

Le thread de mise à jour de jeu gère l’entrée du contrôleur, l’intelligence artificielle et la physique, et prépare les instructions pour les quatre autres threads. Ces instructions sont placées dans des mémoires tampons détenues par le thread de mise à jour de jeu, donc aucune synchronisation n’est requise, car les instructions sont générées.

À la fin du cadre, le thread de mise à jour de jeu transmet les tampons d’instructions aux quatre autres threads, puis commence à travailler sur le frame suivant, en remplissant un autre ensemble de mémoires tampons d’instructions.

Étant donné que les threads de mise à jour et de rendu fonctionnent dans échelons les uns avec les autres, leurs mémoires tampons de communication sont simplement doubles mises en mémoire tampon : à un moment donné, le thread de mise à jour remplit un tampon pendant que le thread de rendu lit à partir de l’autre.

Les autres threads de travail ne sont pas nécessairement liés à la fréquence d’images. La décompression d’un élément de données peut prendre beaucoup moins d’images ou prendre de nombreuses images. Même la simulation de tissu et de cheveux n’a peut-être pas besoin d’être exécutée exactement à la fréquence d’images, car les mises à jour moins fréquentes peuvent être assez acceptables. Par conséquent, ces trois threads ont besoin de structures de données différentes pour communiquer avec le thread de mise à jour et le thread de rendu. Ils ont chacun besoin d’une file d’attente d’entrée qui peut contenir des demandes de travail, et le thread de rendu a besoin d’une file d’attente de données qui peut contenir les résultats produits par les threads. À la fin de chaque frame, le thread de mise à jour ajoute un bloc de demandes de travail aux files d’attente de threads de travail. L’ajout de à la liste une seule fois par trame garantit que le thread de mise à jour minimise la surcharge de synchronisation. Chacun des threads de travail extrait les affectations de la file d’attente de travail aussi rapidement que possible, à l’aide d’une boucle qui ressemble à ceci :


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



Étant donné que les données passent des threads de mise à jour aux threads de travail, puis au thread de rendu, il peut y avoir un délai de trois frames ou plus avant que certaines actions l’affichent à l’écran. Toutefois, si vous attribuez des tâches tolérantes à la latence aux threads de travail, cela ne devrait pas être un problème.

Une conception alternative consisterait à faire en sorte que plusieurs threads de travail dessinent à partir de la même file d’attente de travail. Cela donne un équilibrage de charge automatique et rend plus probable que tous les threads de travail restent occupés.

Le thread de mise à jour de jeu doit veiller à ne pas fournir trop de travail aux threads de travail, sinon les files d’attente de travail peuvent croître en permanence. Le mode de gestion du thread de mise à jour dépend du type de tâches effectuées par les threads de travail.

## <a name="simultaneous-multithreading-and-number-of-threads"></a>Multithread et nombre de threads simultanés

Tous les threads ne sont pas égaux. Deux threads matériels peuvent se trouver sur des puces distinctes, sur le même processeur ou même sur le même noyau. La configuration la plus importante pour les programmeurs de jeu à prendre en compte est de deux threads matériels sur un cœur : la technologie multithreading (SMT) simultanée ou la technologie de Hyper-Threading (HT).

Les threads de technologie SMT ou HT partagent les ressources du cœur de l’UC. Étant donné qu’ils partagent les unités d’exécution, l’accélération maximale de l’exécution de deux threads au lieu d’une est généralement de 10 à 20%, et non pas de 100% par rapport à deux threads matériels indépendants.

Les threads de technologie SMT ou HT partagent plus de manière significative les caches d’instructions et de données L1. Si leurs modèles d’accès à la mémoire sont incompatibles, ils peuvent mettre un terme à la lutte contre le cache et provoquer de nombreux échecs dans le cache. Dans le pire des cas, les performances totales du noyau de l’UC peuvent réellement diminuer lorsqu’un deuxième thread est exécuté. Sur Xbox 360, il s’agit d’un problème relativement simple. La configuration de la Xbox 360 est connue (trois cœurs d’UC chacun avec deux threads matériels) et les développeurs attribuent leurs threads logiciels à des threads d’UC spécifiques et peuvent mesurer pour déterminer si leur conception de threads leur donne des performances supplémentaires.

sur Windows, la situation est plus compliquée. Le nombre de threads et leur configuration varient d’un ordinateur à l’ordinateur, et la détermination de la configuration est compliquée. la fonction [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) fournit des informations sur la relation entre les différents threads matériels, et cette fonction est disponible sur Windows Vista, Windows 7 et Windows XP SP3. Par conséquent, pour l’instant, vous devez utiliser l’instruction CPUID et les algorithmes fournis par Intel et AMD pour décider du nombre de threads « réels » dont vous disposez. Pour plus d’informations, consultez les références.

L’exemple CoreDetection dans le kit de développement logiciel (SDK) DirectX contient un exemple de code qui utilise la fonction [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) ou l’instruction CPUID pour retourner la topologie de base de l’UC. L’instruction CPUID est utilisée si **GetLogicalProcessorInformation** n’est pas pris en charge sur la plateforme actuelle. CoreDetection se trouve aux emplacements suivants :

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Code
</dt> <dd>

*Racine* \\ SDK DirectX Exemples \\ \\ CoreDetection divers \\ C++

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Exécutable
</dt> <dd>

*Racine* \\ SDK DirectX Exemples \\ de \\ \\ casiers divers C++ \\CoreDetection.exe

</dd> </dl>

L’hypothèse la plus sûre consiste à n’avoir qu’un seul thread gourmand en ressources processeur par cœur de processeur. Le fait d’avoir plus de threads nécessitant beaucoup de ressources processeur que les cœurs de processeur offre peu ou pas d’avantages, et augmente la surcharge et la complexité des threads supplémentaires.

## <a name="creating-threads"></a>Création de threads

La création de threads est une opération relativement simple, mais il existe de nombreuses erreurs potentielles. Le code ci-dessous montre la manière appropriée de créer un thread, d’attendre qu’il se termine, puis de le nettoyer.


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



Lorsque vous créez un thread, vous avez la possibilité de spécifier la taille de la pile pour le thread enfant, ou de spécifier zéro, auquel cas le thread enfant hérite de la taille de la pile du thread parent. Sur Xbox 360, où les piles sont entièrement validées lorsque le thread démarre, la spécification de zéro risque de gaspiller de la mémoire importante, car de nombreux threads enfants n’ont pas besoin de la même pile que le parent. Sur la Xbox 360, il est également important que la taille de la pile soit un multiple de 64 Ko.

Si vous utilisez la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour créer des threads, le runtime C/C++ (CRT) ne sera pas correctement initialisé sur Windows. Nous vous recommandons d’utiliser à la place la fonction CRT [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) .

La valeur de retour de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) est un handle de thread. Ce thread peut être utilisé pour attendre que le thread enfant se termine, ce qui est bien plus simple et bien plus efficace que la rotation dans une boucle qui vérifie l’état du thread. Pour attendre que le thread se termine, appelez simplement [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) avec le handle de thread.

Les ressources du thread ne seront pas libérées tant que le thread n’est pas terminé et que le handle de thread n’a pas été fermé. Par conséquent, il est important de fermer le handle de thread avec [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) lorsque vous en avez terminé avec ce dernier. Si vous devez attendre que le thread se termine par [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), veillez à ne pas fermer le descripteur tant que l’attente n’est pas terminée.

Sur Xbox 360, vous devez assigner explicitement des threads logiciels à un thread matériel particulier à l’aide de **XSetThreadProcessor**. Dans le cas contraire, tous les threads enfants resteront sur le même thread matériel que le parent. sur Windows, vous pouvez utiliser [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) pour suggérer fortement au système d’exploitation les threads matériels sur lesquels votre thread doit s’exécuter. cette technique doit généralement être évitée sur Windows, car vous ne savez pas quels autres processus sont en cours d’exécution sur le système. il est généralement préférable de laisser le planificateur de Windows affecter vos threads à des threads matériels inactifs.

La création de threads est une opération coûteuse. Les threads doivent être créés et détruits rarement. Si vous souhaitez créer et détruire des threads fréquemment, utilisez un pool de threads qui attendent un travail à la place.

## <a name="synchronizing-threads"></a>Synchronisation des threads

Pour que plusieurs threads fonctionnent ensemble, vous devez être en mesure de synchroniser des threads, de transmettre des messages et de demander un accès exclusif aux ressources. Windows et Xbox 360 sont fournis avec un ensemble complet de primitives de synchronisation. Pour plus d’informations sur ces primitives de synchronisation, consultez la documentation de la plateforme.

### <a name="exclusive-access"></a>Accès exclusif

Obtenir un accès exclusif à une ressource, à une structure de données ou à un chemin de code est un besoin courant. Une option pour obtenir l’accès exclusif est un mutex, dont l’utilisation typique est indiquée ici.


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



Les sections critiques ont une sémantique similaire aux mutex, mais elles peuvent être utilisées pour synchroniser uniquement au sein d’un processus, et non entre les processus. Leur principal avantage est qu’ils s’exécutent environ vingt fois plus rapidement que les mutex.

### <a name="events"></a>Événements

Si deux threads (peut-être un thread de mise à jour et un thread de rendu) se mettent en forme à l’aide d’une paire de mémoires tampons de description de rendu, elles ont besoin d’un moyen d’indiquer quand elles sont effectuées avec leur mémoire tampon particulière. Pour ce faire, vous pouvez associer un événement (alloué avec [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) à chaque mémoire tampon. Quand un thread est effectué avec une mémoire tampon, il peut utiliser [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent) pour signaler cela et peut ensuite appeler [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) sur l’événement de la mémoire tampon d’autre. Cette technique est facilement extrapolée à la triple mise en mémoire tampon des ressources.

### <a name="semaphores"></a>Sémaphores

Un sémaphore est utilisé pour contrôler le nombre de threads qui peuvent être en cours d’exécution et est couramment utilisé pour implémenter des files d’attente de travail. Un thread ajoute du travail à une file d’attente et utilise [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) chaque fois qu’il ajoute un nouvel élément à la file d’attente. Cela permet de libérer un thread de travail à partir du pool de threads en attente. Les threads de travail appellent simplement [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)et, lorsqu’ils le renvoient, ils savent qu’il y a un élément de travail dans la file d’attente. En outre, une section critique ou une autre technique de synchronisation doit être utilisée afin de garantir un accès sécurisé à la file d’attente de travail partagée.

### <a name="avoid-suspendthread"></a>Éviter SuspendThread

Parfois, lorsque vous souhaitez qu’un thread arrête ce qu’il fait, il est tentant d’utiliser [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) au lieu des primitives de synchronisation correctes. C’est toujours une mauvaise idée et peut facilement entraîner des interblocages et d’autres problèmes. **SuspendThread** interagit également mal avec le débogueur Visual Studio. Évitez le **SuspendThread**. Utilisez à la place [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) .

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject et WaitForMultipleObjects

La fonction [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) est la fonction de synchronisation la plus couramment utilisée. Toutefois, parfois, vous souhaitez qu’un thread attende que plusieurs conditions soient satisfaites simultanément, ou jusqu’à ce que l’un des ensembles de conditions soit respecté. Dans ce cas, vous devez utiliser [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

### <a name="interlocked-functions-and-lockless-programming"></a>Fonctions verrouillées et programmation en bloc

Il existe une famille de fonctions permettant d’effectuer des opérations thread-safe simples sans utiliser de verrous. Il s’agit de la famille de fonctions interverrouillées, telles que [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement). Ces fonctions, ainsi que d’autres techniques qui utilisent un paramètre attentif des indicateurs, sont connues sous le nom de programmation avec verrouillage. La programmation sans verrou peut être extrêmement difficile à effectuer correctement et est beaucoup plus difficile sur Xbox 360 que sur Windows.

Pour plus d’informations sur la programmation sans verrous, consultez Considérations sur la [programmation sans blocage pour Xbox 360 et Microsoft Windows](./lockless-programming.md).

### <a name="minimizing-synchronization"></a>Minimisation de la synchronisation

Certaines méthodes de synchronisation sont plus rapides que d’autres. Toutefois, plutôt que d’optimiser votre code en choisissant les techniques de synchronisation les plus rapides possibles, il est généralement préférable d’effectuer une synchronisation moins fréquente. Cette opération est plus rapide que la synchronisation trop fréquente et facilite le débogage de code plus simple.

Certaines opérations, telles que l’allocation de mémoire, peuvent être amenées à utiliser des primitives de synchronisation pour fonctionner correctement. Par conséquent, les allocations fréquentes à partir du segment de mémoire partagé par défaut entraînent une synchronisation fréquente, ce qui entraîne une perte de performances. Éviter des allocations fréquentes ou utiliser des segments de mémoire par thread (à l’aide du segment de mémoire \_ sans \_ sérialisation si vous utilisez HeapCreate) peut éviter cette synchronisation masquée.

une autre cause de la synchronisation masquée est D3DCREATE \_ multithread, ce qui amène D3D sur Windows à utiliser la synchronisation sur de nombreuses opérations. (L’indicateur est ignoré sur la Xbox 360.)

Les données par thread, également appelées « stockage local des threads », peuvent être un moyen important d’éviter la synchronisation. Visual C++ vous permet de déclarer des variables globales comme étant par thread à l’aide de la syntaxe **\_ \_ declspec (thread)** .


```C++
__declspec( thread ) int tls_i = 1;
```



Cela permet à chaque thread du processus sa propre copie de TLS \_ i, qui peut être référencée en toute sécurité et efficacement sans nécessiter de synchronisation.

La technique **\_ \_ declspec (thread)** ne fonctionne pas avec les DLL chargées dynamiquement. Si vous utilisez des DLL chargées dynamiquement, vous devez utiliser la famille de fonctions TLSAlloc pour implémenter le stockage local des threads.

## <a name="destroying-threads"></a>Destruction de threads

La seule façon sûre de détruire un thread est de quitter le thread, soit en retournant à partir de la fonction de thread principale, soit en faisant en sorte que le thread appelle [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) ou [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx). Si un thread est créé avec [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx), il doit utiliser **\_ endthreadex** ou retourner à partir de la fonction de thread principale, car l’utilisation de **EXITTHREAD** ne libère pas correctement les ressources CRT. N’appelez jamais la fonction [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) , car le thread ne sera pas nettoyé correctement. Les threads doivent toujours valider le suicide, ils ne doivent jamais être Murdered.

## <a name="openmp"></a>OpenMP

OpenMP est une extension de langage qui permet d’ajouter du multithread à votre programme en utilisant des pragmas pour guider le compilateur dans les boucles de parallélisation. OpenMP est pris en charge par Visual C++ 2005 sur Windows et Xbox 360 et peut être utilisé conjointement avec la gestion manuelle des threads. OpenMP peut être un moyen pratique d’effectuer des multithread parties de votre code, mais il est peu probable qu’il s’agit de la solution idéale, en particulier pour les jeux. OpenMP peut être plus applicable aux tâches de production plus longues, telles que le traitement d’art et d’autres ressources. Pour plus d’informations, consultez la documentation Visual C++ ou accédez au [site Web](https://www.openmp.org/)OpenMP.

## <a name="profiling"></a>Profilage

Le profilage multithread est important. Il est facile de se retrouver avec de longues places où les threads sont en attente les uns sur les autres. Ces blocages peuvent être difficiles à trouver et à diagnostiquer. Pour faciliter leur identification, envisagez d’ajouter l’instrumentation à vos appels de synchronisation. Un profileur d’échantillonnage peut également aider à identifier ces problèmes, car il peut enregistrer les informations de minutage sans les modifier sensiblement.

## <a name="timing"></a>Minutage

L’instruction RDTSC est un moyen d’accéder à des informations de temporisation précises sur Windows. Malheureusement, RDTSC présente plusieurs problèmes qui en font un bon choix pour votre titre d’expédition. Les compteurs RDTSC ne sont pas nécessairement synchronisés entre les processeurs. par conséquent, lorsque votre thread se déplace entre les threads matériels, vous pouvez recevoir des différences positives ou négatives importantes. Selon les paramètres de gestion de l’alimentation, la fréquence à laquelle les incréments du compteur RDTSC peuvent également changer au fur et à mesure de l’exécution de votre jeu. Pour éviter ces difficultés, vous devez préférer [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) et [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) pour une synchronisation à haute précision dans votre jeu d’expédition. Pour plus d’informations sur la synchronisation, consultez la page relative au [minutage des jeux et aux processeurs multicœurs](./game-timing-and-multicore-processors.md).

## <a name="debugging"></a>Débogage

Visual Studio prend entièrement en charge le débogage multithread pour Windows et Xbox 360. la fenêtre Visual Studio threads vous permet de basculer entre les threads afin de voir les différentes piles d’appels et variables locales. La fenêtre threads vous permet également de figer et de libérer des threads particuliers.

Sur Xbox 360, vous pouvez utiliser la variable méta **\@ hwthread** dans la fenêtre Espion pour afficher le thread matériel sur lequel le thread logiciel actuellement sélectionné est en cours d’exécution.

La fenêtre threads est plus facile à utiliser si vous nommez vos threads de manière significative. Visual Studio et d’autres débogueurs Microsoft vous permettent de nommer vos threads. Implémentez la fonction **SetThreadName** suivante et appelez-la à partir de chaque thread au démarrage.


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



Le débogueur de noyau (KD) et WinDBG prennent également en charge le débogage multithread.

## <a name="testing"></a>Test

La programmation multithread peut être délicate et certains bogues multithreads s’affichent rarement, ce qui les rend difficiles à trouver et à corriger. L’une des meilleures façons de les vider consiste à effectuer des tests sur un large éventail d’ordinateurs, en particulier ceux avec quatre processeurs ou plus. Le code multithread qui fonctionne parfaitement sur un ordinateur à thread unique peut échouer instantanément sur un ordinateur à quatre processeurs. Les caractéristiques de performances et de minutage des processeurs AMD et Intel peuvent varier considérablement. Veillez donc à tester sur les ordinateurs multiprocesseurs basés sur les processeurs des deux fournisseurs.

## <a name="windows-vista-and-windows-7-improvements"></a>Windows améliorations apportées à Vista et Windows 7

pour les jeux ciblant les versions plus récentes de Windows, il existe un certain nombre d’api qui peuvent simplifier la création d’applications multithread évolutives. Cela est particulièrement vrai avec la nouvelle API ThreadPool et certaines primitives syncrhonziation supplémentaires (variables de condition, verrou de lecture/écriture allégé et initialisation unique). Vous trouverez une vue d’ensemble de ces technologies dans les articles suivants du magazine MSDN :

-   [Améliorez l’évolutivité avec les nouvelles API de pool de threads](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [nouvelles primitives de synchronisation pour Windows Vista](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

Les applications utilisant les [fonctionnalités Direct3D 11](../direct3d11/direct3d-11-features.md) sur ces systèmes d’exploitation peuvent également tirer parti de la nouvelle conception pour la création d’objets simultanés et des listes de commandes de contexte différées pour une meilleure évolutivité pour le rendu multithread.

## <a name="summary"></a>Résumé

Avec une conception minutieuse qui minimise les interactions entre les threads, vous pouvez bénéficier de gains de performances substantiels de la programmation multithread sans ajouter une complexité excessive à votre code. Cela permet à votre code de jeu d’ignorer la prochaine vague d’améliorations du processeur et de fournir des expériences de jeux plus attrayantes.

## <a name="references"></a>Références

-   Jim Beveridge & Robert Weiner, *applications multithread dans Win32*, Addison-Wesley, 1997
-   Chuck Walbourn, [minutage des jeux et processeurs multicœurs](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005
-   Bibliothèque MSDN : [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 