---
title: programmation 64 bits pour les développeurs de jeux
description: Cet article traite des problèmes de compatibilité et de Portage et aide les développeurs à faciliter leur transition vers des plateformes 64 bits.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e57ea1b3cc3272ca40465df31a04244d99e68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031561"
---
# <a name="64-bit-programming-for-game-developers"></a>programmation 64 bits pour les développeurs de jeux

Les fabricants de processeurs expédient exclusivement des processeurs 64 bits sur leurs ordinateurs de bureau, et même les chipsets de la plupart des ordinateurs portables prennent en charge la technologie x64. Il est important pour les développeurs de jeux de tirer parti des améliorations apportées par les processeurs 64 bits avec leurs nouvelles applications et de s’assurer que leurs applications antérieures s’exécutent correctement sur les nouveaux processeurs et les éditions 64 bits de Windows Vista et Windows 7. Cet article traite des problèmes de compatibilité et de Portage et aide les développeurs à faciliter leur transition vers des plateformes 64 bits.

Microsoft possède actuellement les systèmes d’exploitation 64 bits suivants :

-   Windows Server 2003 Service Pack 1
-   Windows XP Professionnel Édition x64 (disponible pour les fabricants d’ordinateurs OEM et les développeurs via MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 est uniquement disponible en version 64 bits.

 

-   [Différences dans la mémoire adressable](#differences-in-addressable-memory)
-   [Spécification de la prise en charge des adresses importantes lors de la génération](#specifying-large-address-aware-when-building)
-   [Compatibilité des applications 32 bits sur les plateformes 64 bits](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Pièges de compatibilité potentiels](#potential-compatibility-pitfalls)
-   [Portage d’applications vers des plateformes 64 bits](#porting-applications-to-64-bit-platforms)
-   [Profilage et optimisation des applications portées](#profiling-and-optimization-of-ported-applications)
-   [Code managé sur un système d’exploitation 64 bits](#managed-code-on-a-64-bit-operating-system)
-   [Implications sur les performances de l’exécution d’un système d’exploitation 64 bits](#performance-implications-of-running-a-64-bit-operating-system)
-   [Résumé](#summary)

## <a name="differences-in-addressable-memory"></a>Différences dans la mémoire adressable

La première chose que la plupart des développeurs remarquent est que les processeurs 64 bits fournissent un énorme bond dans la quantité de mémoire physique et virtuelle qui peut être traitée.

-   les applications 32 bits sur les plateformes 32 bits peuvent traiter jusqu’à 2 Go.
-   les applications 32 bits générées avec l’indicateur d’éditeur de liens/LARGEADDRESSAWARE : YES sur 32 bits Windows XP ou Windows Server 2003 avec l’option de démarrage/3GB spéciale peuvent traiter jusqu’à 3 Go. Cela limite le noyau à 1 Go, ce qui peut entraîner l’échec de certains pilotes et/ou services.
-   les applications 32 bits générées avec l’indicateur d’éditeur de liens/LARGEADDRESSAWARE : YES sur les éditions 32 bits de Windows Vista, Windows Server 2008 et Windows 7 peuvent traiter la mémoire jusqu’au nombre spécifié par l’élément de données de configuration de démarrage (BCD) IncreaseUserVa. IncreaseUserVa peut avoir une valeur comprise entre 2048, la valeur par défaut, 3072 (qui correspond à la quantité de mémoire configurée par l’option de démarrage/3GB sur Windows XP). Le reste de 4 Go est alloué au noyau et peut entraîner l’échec des configurations du pilote et du service.

    Pour plus d’informations sur BCD, consultez [données de configuration de démarrage (BCD)](https://msdn.microsoft.com/library/aa362692.aspx) sur MSDN.

-   les applications 32 bits sur les plateformes 64 bits peuvent adresser jusqu’à 2 Go, ou jusqu’à 4 Go avec l’indicateur d’éditeur de liens/LARGEADDRESSAWARE : YES.
-   les applications 64 bits utilisent 43 bits pour l’adressage, qui fournit 8 to d’adresse virtuelle pour les applications et 8 to réservés pour le noyau.

Au-delà de la mémoire, les applications 64 bits qui utilisent l’avantage d’e/s de fichier mappé en mémoire sont largement tirées de l’espace d’adressage virtuel accru. L’architecture 64 bits offre également des performances à virgule flottante améliorées et une transmission plus rapide des paramètres. Les processeurs 64 bits ont un double du nombre de registres, des types à usage général et des extensions streaming SIMD (SSE), ainsi que la prise en charge des jeux d’instructions SSE et SSE2 ; de nombreux processeurs 64 bits prennent même en charge les jeux d’instructions SSE3.

## <a name="specifying-large-address-aware-when-building"></a>Spécification de la prise en charge des adresses importantes lors de la génération

Il est recommandé de spécifier la prise en charge des adresses importantes lors de la génération d’applications 32 bits, à l’aide de l’indicateur de l’éditeur de liens/LARGEADDRESSAWARE, même si l’application n’est pas destinée à une plateforme 64 bits, en raison des avantages acquis gratuitement. Comme expliqué précédemment, l’activation de cet indicateur pour une build permet à un programme 32 bits d’accéder à davantage de mémoire avec des options de démarrage spéciales sur un système d’exploitation 32 bits ou sur un système d’exploitation 64 bits. Toutefois, les développeurs doivent veiller à ce que les hypothèses de pointeur ne soient pas faites, par exemple en supposant que le bit de poids fort n’est jamais défini dans un pointeur 32 bits. En général, l’activation de l’indicateur/LARGEADDRESSAWARE est une bonne pratique.

Les applications 32 bits qui prennent en charge les adresses peuvent déterminer au moment de l’exécution la quantité d’espace d’adressage virtuel totale qui leur est disponible avec la configuration actuelle du système d’exploitation en appelant [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex). Le résultat ullTotalVirtual est compris entre 2147352576 octets (2 Go) et 4294836224 octets (4 Go). Les valeurs supérieures à 3221094400 (3 Go) peuvent uniquement être obtenues sur les éditions 64 bits de Windows. Par exemple, si IncreaseUserVa a la valeur 2560, le résultat est ullTotalVirtual avec une valeur de 2684223488 octets.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Compatibilité des applications 32 bits sur les plateformes 64 bits

Les systèmes d’exploitation Windows 64 bits sont compatibles binaires avec l’architecture IA32, et la majorité des API utilisées par les applications 32 bits sont disponibles via Windows 32 bits sur l’émulateur Windows 64 bits, WOW64. WOW64 permet de s’assurer que ces API fonctionnent comme prévu.

WOW64 a une couche d’exécution qui gère le marshaling des données 32 bits. WOW64 redirige les demandes de fichier DLL, redirige certaines branches du Registre pour les applications 32 bits et reflète certaines branches du Registre pour les applications 32 et 64 bits.

Pour plus d’informations sur WOW64, consultez les détails de l' [implémentation WOW64](/windows/desktop/WinProg64/wow64-implementation-details) sur MSDN. Pour connaître les meilleures pratiques pour la création d’applications qui s’exécutent sur WOW64, consultez [meilleures pratiques pour WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) sur Windows Hardware Developer Central.

### <a name="potential-compatibility-pitfalls"></a>Pièges de compatibilité potentiels

La plupart des applications développées pour une plateforme 32 bits s’exécuteront sans problème sur une plateforme 64 bits. Certaines applications peuvent présenter des problèmes, notamment les suivants :

-   Tous les pilotes pour les éditions 64 bits des systèmes d’exploitation Windows doivent être des versions 64 bits. L’exigence de nouveaux pilotes 64 bits a des implications pour les schémas de protection contre la copie qui reposent sur les anciens pilotes. Notez que les pilotes en mode noyau doivent être signés par Authenticode pour être chargés par les éditions 64 bits de Windows.
-   les processus 64 bits ne peuvent pas charger les dll 32 bits, et les processus 32 bits ne peuvent pas charger les dll 64 bits. Les développeurs doivent s’assurer que les versions 64 bits des dll tierces sont disponibles avant de procéder au développement. Si vous devez utiliser une DLL 32 bits dans un processus 64 bits, la communication entre processus Windows (IPC) peut être utilisée. Les composants COM peuvent également utiliser les serveurs hors processus et le marshaling pour communiquer entre les limites, mais cela peut entraîner une baisse des performances.
-   De nombreux processeurs x64 sont également des processeurs multicœurs, et les développeurs doivent tester la manière dont cela affecte leurs applications héritées. Vous trouverez plus d’informations sur les processeurs multicœurs et les implications pour les applications de jeu dans les [processeurs de synchronisation de jeux et multicœurs](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).
-   Les applications doivent également appeler [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) pour découvrir les chemins d’accès aux fichiers, car certains noms de dossiers ont été modifiés dans certains cas. Par exemple, les \_ fichiers programme CSIDL \_ retournent « C : \\ Program Files (x86) » pour une application 32 bits qui s’exécute sur une plateforme 64 bits au lieu de « c : \\ Program Files ». Les développeurs doivent être attentifs à la façon dont les fonctionnalités de redirection et de réflexion de l’émulateur WOW64 fonctionnent.

En outre, les développeurs doivent être vigilants avec les programmes 16 bits qu’ils utilisent peut-être encore. WOW64 ne peut pas gérer les applications 16 bits. Cela comprend les anciens programmes d’installation et tous les programmes MS-DOS.

> [!Note]  
> Les problèmes de compatibilité les plus courants sont les programmes d’installation qui exécutent du code 16 bits et qui n’ont pas de pilotes 64 bits pour les schémas de protection contre la copie.

 

La section suivante traite des problèmes liés au portage de code vers le mode natif 64 bits pour les développeurs qui souhaitent s’assurer que leurs programmes hérités fonctionnent sur des plateformes 64 bits. C’est également pour les développeurs qui ne connaissent pas la programmation 64 bits.

## <a name="porting-applications-to-64-bit-platforms"></a>Portage d’applications vers des plateformes 64 bits

Le fait de disposer des bons outils et bibliothèques vous aidera à faciliter la transition du développement 32 bits à 64 bits. Le kit de développement logiciel (SDK) DirectX 9 contient des bibliothèques qui prennent en charge les projets x86 et x64. Microsoft Visual Studio 2005 et Visual Studio 2008 prennent en charge la génération de code pour x86 et x64, et elles sont fournies avec des bibliothèques optimisées pour la génération de code x64. Toutefois, il est également nécessaire pour les développeurs de distribuer les runtimes Visual C avec leurs applications. Notez que les éditions Express de Visual Studio 2005 et Visual Studio 2008 n’incluent pas le compilateur x64, contrairement aux éditions standard, Professional et Team System.

Les développeurs qui ciblent des plateformes 32 bits peuvent préparer le développement 64 bits pour faciliter la transition plus tard. Lors de la compilation de projets 32 bits, les développeurs doivent utiliser l’indicateur/Wp64, ce qui entraîne la génération d’avertissements sur les problèmes affectant la portabilité. Le basculement vers les outils et les bibliothèques 64 bits générera probablement beaucoup de nouvelles erreurs de génération. par conséquent, il est recommandé de basculer entre les outils et les bibliothèques de bits neutres et de corriger les avertissements avant de passer à une version 64 bits.

Toutefois, la modification des outils, la modification des bibliothèques et l’utilisation de certains indicateurs du compilateur ne suffisent pas. Les hypothèses dans les normes de codage doivent être réévaluées pour s’assurer que les normes de codage actuelles n’autorisent pas les problèmes de portabilité. Les problèmes de portabilité peuvent inclure la troncation de pointeur, la taille et l’alignement des types de données, la dépendance sur les dll 32 bits, l’utilisation d’API héritées, le code assembleur et les anciens fichiers binaires.

> [!Note]  
> Visual C++ 2010 comprend les en-têtes stdint. h et cstdint C99 qui définissent les types de portabilité standard Int32 \_ t, UInt32 \_ t, Int64 \_ t, UInt64 \_ t, IntPtr \_ t et UIntPtr \_ t. L’utilisation de ceux-ci avec les types de données standard ptrdiff \_ t et Size \_ t peut être préférable aux types Windows portabilty utilisés ci-dessous pour améliorer la portabilité du code.

 

Les principaux problèmes de Portage sont les suivants :

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Troncation de pointeur**
</dt> <dd>

Les pointeurs étant de 64 bits sur un système d’exploitation 64 bits, le cast de pointeurs vers d’autres types de données peut entraîner une troncation, et l’arithmétique de pointeur peut entraîner une altération. L’utilisation de l’indicateur/Wp64 fournit généralement un avertissement sur ce type de problème, mais l’utilisation de types polymorphes (INT \_ ptr, DWORD \_ ptr, size \_ T, uint \_ ptr, etc.) lors de la conversion des types pointeur est une bonne pratique pour éviter tout problème. Étant donné que les pointeurs sont 64 bits sur les nouvelles plateformes, les développeurs doivent vérifier l’ordre des pointeurs, ainsi que les types de données dans les classes et les structures, afin de réduire ou d’éliminer le remplissage.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Types de données et fichiers binaires**
</dt> <dd>

Alors que les pointeurs augmentent de 32 bits à 64 sur une plateforme 64 bits, les autres types de données ne le sont pas. Les types de données à précision fixe (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32, UINT64) peuvent être utilisés dans des emplacements où la taille du type de données doit être connue. par exemple, dans une structure de fichiers binaires. Les modifications apportées à la taille du pointeur et à l’alignement des données nécessitent un traitement spécial pour garantir la compatibilité 32 bits-à 64-bit. Pour plus d’informations, consultez [préparation pour Windows 64 bits : nouveaux types de données](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**Anciennes API Win32 et alignement des données**
</dt> <dd>

Certaines API Win32 ont été dépréciées et remplacées par des appels d’API plus neutres tels que SetWindowLongPtr à la place de SetWindowLong.

La baisse des performances pour les accès non alignés est plus importante sur la plateforme x64 que sur une plateforme x86. Les \_ macros alignement de type (t) et décalage de champ \_ (t, membre) peuvent être utilisées pour déterminer les informations d’alignement qui peuvent être utilisées directement par le code. L’utilisation correcte de ces macros mentionnées ci-dessus doit éliminer les pénalités potentielles d’accès non aligné.

Pour plus d’informations sur la macro d’alignement de TYPE \_ , la \_ macro décalage de champ et les informations de programmation 64 bits générales, consultez [programmation Windows sur 64 bits : conseils de migration : considérations supplémentaires](/windows/desktop/WinProg64/additional-considerations) et [préparation pour les fenêtres 64 bits : règles d’utilisation des pointeurs](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Code assembleur**
</dt> <dd>

Le code assembleur inline n’est pas pris en charge sur les plateformes 64 bits et doit être remplacé. Les modifications apportées à l’architecture peuvent avoir changé les goulots d’étranglement de l’application, et C/C++ ou intrinsèques peuvent obtenir des résultats similaires avec un code plus facile à lire. La pratique la plus recommandée consiste à basculer tout le code d’assembly vers C ou C++. Les intrinsèques peuvent être utilisés à la place du code assembleur, mais ne doivent être utilisés qu’après l’exécution du profilage et de l’analyse complets.

X87, MMX et 3DNow ! les jeux d’instructions sont déconseillés en mode 64 bits. Les ensembles d’instructions sont toujours présents pour la compatibilité descendante en mode 32 bits ; Toutefois, pour éviter des problèmes de compatibilité à l’avenir, leur utilisation dans les projets actuels et futurs est déconseillée.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**API déconseillées**
</dt> <dd>

Certaines API DirectX plus anciennes ont été supprimées pour les applications natives 64 bits : DirectPlay 4 et versions antérieures, DirectDraw 6 et versions antérieures, Direct3D 8 et versions antérieures, et DirectInput 7 et versions antérieures. En outre, l’API principale de DirectMusic est disponible pour les applications 64 bits natives, mais la couche de performances et le producteur DirectMusic sont déconseillés.

Visual Studio émet des avertissements de désapprobation, et ces modifications ne sont pas un problème pour les développeurs qui utilisent les API les plus récentes.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Profilage et optimisation des applications portées

Tous les développeurs doivent reprofiler toutes les applications qui sont portées vers de nouvelles architectures. De nombreuses applications qui sont portées sur des plateformes 64 bits auront des profils de performances différents de leurs versions 32 bits. Les développeurs doivent exécuter des tests de performances 64 bits avant d’évaluer ce qui doit être optimisé. La bonne nouvelle à ce sujet est que de nombreuses optimisations traditionnelles fonctionnent sur des plateformes 64 bits. En outre, les compilateurs 64 bits peuvent également effectuer de nombreuses optimisations avec l’utilisation correcte des indicateurs de compilateur et des indicateurs de codage.

Certaines structures peuvent avoir leurs types de données internes réorganisés pour économiser l’espace mémoire et améliorer la mise en cache. Les index de tableau peuvent être utilisés à la place d’un pointeur 64 bits complet dans certains cas. L’indicateur/FP : Fast peut améliorer l’optimisation et la vectorisation à virgule flottante. L’utilisation \_ \_ de la restriction, declspec (restrict) et declspec (noalias) peut aider le compilateur à résoudre les alias et à améliorer l’utilisation du fichier de registre.

Vous trouverez plus d’informations sur/FP : Fast sur [/FP (spécifier le comportement de Floating-Point)](/cpp/build/reference/fp-specify-floating-point-behavior).

Pour plus d’informations sur \_ \_ restrict [, consultez modificateurs spécifiques à Microsoft](/cpp/cpp/microsoft-specific-modifiers).

Pour plus d’informations sur declspec (restrict), consultez [meilleures pratiques](/cpp/build/optimization-best-practices)pour l’optimisation.

Vous trouverez plus d’informations sur declspec (noalias) dans [ \_ \_ declspec (noalias)](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx).

## <a name="managed-code-on-a-64-bit-operating-system"></a>Code managé sur un système d’exploitation 64 bits

Le code managé est utilisé par de nombreux développeurs de jeux dans leur chaîne d’outils. ainsi, une bonne compréhension de son comportement sur un système d’exploitation 64 bits peut être utile. Le code managé est un jeu d’instructions neutre. par conséquent, lorsque vous exécutez une application managée sur un système d’exploitation 64 bits, le Common Language Runtime (CLR) peut l’exécuter en tant que processus 32 bits ou 64 bits. Par défaut, le CLR exécute des applications gérées en tant que 64 bits et ne fonctionne pas correctement. Toutefois, si votre application dépend d’une DLL native 32 bits, votre application échouera lorsqu’elle tentera d’appeler cette DLL. Un processus 64 bits a besoin d’un code entièrement 64 bits, et une DLL 32 bits ne peut pas être appelée à partir d’un processus de 64 bits. La meilleure solution à long terme consiste à compiler votre code natif comme 64-bit également, mais une solution parfaitement raisonnable à long terme consiste simplement à marquer votre application gérée comme étant pour x86 uniquement à l’aide de l’indicateur de build/Platform : x86.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Implications sur les performances de l’exécution d’un système d’exploitation 64 bits

Étant donné que les processeurs dotés de l’architecture AMD64 et Intel 64 peuvent exécuter des instructions 32 bits en mode natif, ils peuvent exécuter des applications 32 bits à pleine vitesse, même sur un système d’exploitation de 64 bits. Il existe un coût modeste pour la conversion des paramètres entre 32 bits et 64 bits lors de l’appel de fonctions du système d’exploitation, mais ce coût est généralement négligeable. Cela signifie que vous ne devriez voir aucun ralentissement lors de l’exécution d’applications 32 bits sur un système d’exploitation 64 bits.

Lorsque vous compilez des applications en tant que 64 bits, les calculs sont plus compliqués. Un programme 64 bits utilise des pointeurs 64 bits, et ses instructions sont légèrement plus grandes, donc la mémoire requise est légèrement augmentée. Cela peut entraîner une légère baisse des performances. D’un autre côté, le fait d’avoir deux fois plus de registres et d’avoir la possibilité d’effectuer des calculs d’entiers 64 bits dans une instruction unique est souvent plus que compenser. Le résultat net est qu’une application 64 bits peut s’exécuter légèrement plus lentement que la même application compilée en tant que 32 bits, mais elle s’exécute souvent un peu plus rapidement.

## <a name="summary"></a>Résumé

Les architectures 64 bits permettent aux développeurs de pousser les limites sur la façon dont les jeux s’affichent, le son et les jouent. Toutefois, la transition de la programmation 32 bits à la programmation 64 bits n’est pas évidente. En comprenant les différences entre les deux, et en utilisant les outils les plus récents, la transition vers les plateformes 64 bits peut être plus facile et plus rapide.

Vous trouverez plus d’informations sur la programmation 64 bits dans [Visual C++ Centre de développement : programmation 64 bits](https://msdn.microsoft.com/vstudio//aa336463.aspx).

 

 