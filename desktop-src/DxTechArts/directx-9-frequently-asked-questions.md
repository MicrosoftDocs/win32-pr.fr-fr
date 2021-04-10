---
title: Forum aux questions DirectX
description: Cet article contient une série de questions fréquemment posées (FAQ) sur Microsoft DirectX.
ms.assetid: 58d9fe45-a2c7-8280-2826-e2e14ecea983
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd5fd70f1a651121b8d977dbb9479cef6edd024
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031521"
---
# <a name="directx-frequently-asked-questions"></a>Forum aux questions DirectX

Cet article contient une série de questions fréquemment posées (FAQ) sur Microsoft DirectX.

-   [Problèmes généraux de développement DirectX](#general-directx-development-issues)
-   [Questions sur Direct3D](#direct3d-questions)
    -   [Questions générales sur Direct3D](#general-direct3d-questions)
    -   [Traitement Geometry (vertex)](#geometry-vertex-processing)
    -   [Réglage des performances](#performance-tuning)
    -   [Bibliothèque de l’utilitaire D3DX](#d3dx-utility-library)
-   [Questions sur DirectSound](#directsound-questions)
-   [Extensions DirectX pour Alias Maya](#directx-extensions-for-alias-maya)
-   [Questions XInput](#xinput-questions)

## <a name="general-directx-development-issues"></a>Problèmes généraux de développement DirectX

<dl> <dt>

<span id="Should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="SHOULD_GAME_DEVELOPERS_REALLY_CARE_ABOUT_SUPPORTING_X64_EDITIONS_"></span>**Les développeurs de jeux doivent-ils s’intéresser à la prise en charge des éditions x64 ?**
</dt> <dd>

Absolument. la technologie x64 est largement disponible sur le marché. La majorité des nouveaux processeurs vendus au cours des dernières années, et presque toutes les lignes de processeur en développement d’AMD et d’Intel, sont conformes à la technologie x64. Windows XP Professionnel Édition x64 a introduit la technologie d’activation du système d’exploitation pour x64 publiée en avril de 2005. Étant donné que les éditions x64 requièrent une nouvelle génération de pilotes natifs 64 bits, cette première version était limitée à la distribution OEM.

Avec Windows Vista, les clients sont libres de choisir les éditions 32 bits ou 64 bits lors de l’achat d’ordinateurs Windows, et les licences pour Windows Vista sont valides pour les éditions 32 bits ou 64 bits du système d’exploitation. En outre, de nombreux pilotes 64 bits sont disponibles dans la zone, et les fabricants de périphériques sont requis pour fournir des pilotes natifs 32 bits et 64 bits dans le cadre du programme de certification Windows.

Tous ces facteurs augmentent de façon considérable les déploiements des éditions 64 bits de Windows. À mesure que les nouveaux ordinateurs commencent à être livrés avec plus de 2 Go de RAM physique, l’incentive pour utiliser un système d’exploitation 32 bits diminue de manière importante en faveur des éditions 64 bits. La technologie 64 bits prend entièrement en charge le code natif 32 bits, bien que les implémentations natives de 64 bits soient nécessaires pour tirer pleinement parti du nouvel espace mémoire de 64 bits. Chaque application 32 bits doit avoir une compatibilité avec 64 bits comme condition d’expédition minimale et répondre à cette exigence est un impératif de base pour la compatibilité avec Windows Vista. En général, les incompatibilités proviennent de l’utilisation d’un code 16 bits conçu pour le système d’exploitation Windows 3,1 ou de l’installation de pilotes qui ne sont pas fournis à la fois sous forme native 32 bits et 64 bits.

Pour plus d’informations sur la technologie 64 bits, consultez la page [programmation 64 bits pour les développeurs de jeux](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_95__Windows_98_or_Windows_ME_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_95__windows_98_or_windows_me_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_95__WINDOWS_98_OR_WINDOWS_ME_"></span>**Les développeurs de jeux doivent-ils toujours publier des jeux pour Windows 95, Windows 98 ou Windows ME ?**
</dt> <dd>

Plus pour deux raisons : performances et ensemble de fonctionnalités.

Si la vitesse d’UC minimale requise pour votre jeu est 1,2 GHz ou plus (ce qui est plus courant pour les titres à hautes performances), la grande majorité des ordinateurs éligibles exécute Windows XP. Par le moment où les ordinateurs avec une vitesse de processeur supérieure à 1,2 GHz étaient vendus, Windows XP a été installé en tant que système d’exploitation par défaut par presque tous les fabricants. Cela signifie qu’il existe de nombreuses fonctionnalités disponibles dans Windows XP, que les développeurs de jeux actuels doivent tirer parti des éléments suivants :

-   Amélioration des tâches multitâches, ce qui se traduit par une expérience plus lisse pour la vidéo, l’audio et les jeux.
-   Modèle de pilote vidéo plus stable, qui permet un débogage plus facile, un jeu plus lisse et de meilleures performances.
-   Configuration plus facile pour la mise en réseau, qui permet un accès plus facile aux jeux multi-joueurs.
-   Prise en charge des transferts DMA par défaut à partir de disques durs, ce qui entraîne un chargement plus rapide et plus rapide des applications.
-   Rapport d’erreurs Windows, ce qui aboutit à un système d’exploitation, des pilotes et des applications plus stables.
-   Prise en charge d’Unicode, ce qui simplifie grandement les problèmes de localisation.
-   Amélioration de la sécurité et de la stabilité, ce qui a pour résultat une meilleure expérience utilisateur.
-   Meilleure prise en charge du matériel moderne, qui n’utilise plus les pilotes Windows 98.
-   Amélioration de la gestion de la mémoire, ce qui améliore la stabilité et la sécurité.
-   Système de fichiers NTFS amélioré, ce qui est plus résistant aux défaillances et offre de meilleures performances avec des fonctionnalités de sécurité.

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_2000_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_2000_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_2000_"></span>**Les développeurs de jeux doivent-ils toujours publier des jeux pour Windows 2000 ?**
</dt> <dd>

Plus maintenant. En plus des raisons indiquées dans, **les développeurs de jeux sont-ils toujours en mesure de publier des jeux pour windows 95, windows 98 ou Windows me ?**, Windows 2000 ne dispose pas des fonctionnalités suivantes :

-   Windows XP prend en charge des fonctionnalités de processeur avancées, telles que l’Hyper-Threading, le multicœur et x64.
-   Windows XP prend en charge les composants côte à côte, ce qui réduit considérablement les conflits de contrôle de version de l’application.
-   Windows XP prend en charge la protection de la mémoire sans exécution qui permet d’empêcher les programmes malveillants et peut aider au débogage.
-   Windows XP a amélioré la prise en charge des cartes vidéo avancées AGP et PCI Express.
-   Windows XP prend en charge le changement rapide d’utilisateur, le Bureau à distance et l’assistance à distance, ce qui peut aider à réduire les coûts de support produit.
-   Les outils de performances comme PIX (dans le kit de développement logiciel (SDK) développeur DirectX) ne prennent plus en charge Windows 2000.

En bref, Windows 2000 n’a jamais été conçu ou commercialisé comme un système d’exploitation consommateur.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_Vista__How_do_they_impact_my_DirectX_application_"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_vista__how_do_they_impact_my_directx_application_"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_VISTA__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION_"></span>**Quelles sont les différences entre les différentes éditions de Windows Vista ? Comment les impactent-ils sur mon application DirectX ?**
</dt> <dd>

La famille Windows Vista comprend cinq éditions :

-   Windows Vista Édition Familiale Basique
-   Windows Vista Édition Familiale Premium
-   Windows Vista Professionnel
-   Windows Vista Entreprise
-   Windows Vista Édition Intégrale

Édition familiale basique et édition familiale Premium sont des versions axées sur les consommateurs, avec des fonctionnalités telles que la sécurité des familles (anciennement appelées contrôles parental) et la version Premium Premium comprend Media Center. L’entreprise et l’entreprise sont des éditions axées sur l’entreprise, avec des fonctionnalités telles que la jonction de domaine et les Bureau à distance/services Terminal Server. L’édition intégrale combine toutes les fonctionnalités des éditions Consumer et Corporate en une seule version. Toutes les éditions sont disponibles à la fois dans les éditions 32 bits (x86) et 64 bits (x64), et les utilisateurs sont libres d’utiliser le même identificateur de produit pour les deux plateformes.

La technologie sous-jacente aux différentes éditions est identique et elles ont toutes la même version du runtime DirectX et d’autres composants. Toutefois, les éditions présentent quelques différences mineures par rapport aux jeux :

-   L’Explorateur de jeux existe dans toutes les éditions, mais le raccourci jeux dans le menu Démarrer est uniquement dans édition familiale basique, édition familiale Premium et édition intégrale. L’Explorateur de jeux peut toujours être trouvé dans toutes les éditions (en cliquant sur Démarrer, en pointant sur tous les programmes, puis en cliquant sur jeux) et les fonctions de l’interface IGameExplorer sur toutes les éditions.
-   Les jeux inclus avec Windows ne sont pas disponibles par défaut sur l’entreprise et l’entreprise, mais ils peuvent être activés par l’administrateur.
-   La sécurité des familles et les évaluations des jeux n’affichent pas ou n’ont aucune incidence sur le comportement de l’entreprise ou de l’entreprise, et elles sont désactivées sur le niveau optimal lorsqu’un domaine est joint.

Les paramètres de contrôle de compte d’utilisateur ont les mêmes valeurs par défaut pour toutes les éditions, mais ils peuvent être remplacés par stratégie de groupe paramètres du domaine sur entreprise, entreprise et édition intégrale. Par exemple, le paramètre de stratégie contrôle de compte d’utilisateur : comportement de l’invite d’élévation pour les utilisateurs standard peut être configuré pour refuser automatiquement les demandes d’élévation dans de nombreux paramètres d’entreprise afin d’améliorer la sécurité, et de nombreux utilisateurs dans ces environnements s’exécuteront toujours en tant qu’utilisateurs standard sans pouvoir même choisir d’exécuter en tant qu’administrateur. Tout programme (tel qu’un programme d’installation) qui requiert des droits d’administration, en raison de la détection d’installation héritée ou de la présence d’un manifeste qui spécifie le niveau d’exécution demandé sur « requireAdministrator », échouera toujours dans de telles situations. D’autres paramètres de stratégie, tels que le contrôle de compte d’utilisateur : élever uniquement les exécutables signés et validés, peuvent également empêcher le bon fonctionnement de votre programme d’installation si vous ne signez pas votre fichier exécutable à l’aide d’Authenticode.

Ces types de modifications de stratégie peuvent être appliqués à n’importe quelle édition de Windows Vista, mais elles sont plus probables sur les ordinateurs qui sont joints à un domaine.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_7__How_do_they_impact_my_DirectX_application__"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_7__how_do_they_impact_my_directx_application__"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_7__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION__"></span>**Quelles sont les différences entre les différentes éditions de Windows 7 ? Comment les impactent-ils sur mon application DirectX ?** 
</dt> <dd>

La majorité des utilisateurs de Windows 7 auront probablement l’une des deux éditions suivantes : Windows 7 Édition familiale Premium, pour les particuliers ou Windows 7 professionnel, pour les utilisateurs professionnels et les développeurs. Pour les grandes entreprises, l’édition Windows 7 entreprise avec licence en volume inclut toutes les fonctionnalités de Windows 7. Windows 7 édition intégrale est l’équivalent au détail de cette édition.

Windows 7 Édition Starter est disponible dans le monde entier pour les fabricants OEM et doit être déployé principalement avec les netlivres, les ordinateurs portables ultra-faiblement alimentés. Windows 7 édition personnelle est disponible uniquement sur les marchés émergents.

Notez que toutes les éditions de Windows 7 (à l’exception de l’édition Starter) sont disponibles pour les versions 32 bits (x86) et 64 bits (x64), et que tous les packages de vente au détail de Windows 7 incluent le média pour les deux versions. Comme avec Windows Vista, les utilisateurs sont libres d’utiliser le même identificateur de produit commercialisé sur l’une ou l’autre des plateformes.

La technologie sous-jacente dans les différentes éditions est identique et toutes les éditions ont la même version du runtime DirectX et d’autres composants. Ils présentent quelques différences en ce qui concerne les fonctionnalités de jeux :

-   L’Explorateur de jeux existe dans toutes les éditions, mais le raccourci jeux dans le menu Démarrer est masqué par défaut dans Windows 7 professionnel et entreprise. L’Explorateur de jeux est toujours disponible dans le menu Démarrer (en cliquant sur tous les programmes, puis en double-cliquant sur jeux) et le raccourci direct Games peut être activé par l’utilisateur.
-   Les jeux inclus avec Windows ne sont pas disponibles par défaut sur Windows 7 professionnel et entreprise, mais ils peuvent être activés par l’administrateur.
-   La sécurité des familles et les évaluations des jeux sont disponibles dans toutes les éditions, mais elles sont désactivées sur Windows 7 professionnel, entreprise et édition intégrale quand le système d’exploitation rejoint un domaine. Comme avec Windows Vista Édition intégrale, cette fonctionnalité peut être réactivée sur un ordinateur qui a rejoint un domaine.

Les paramètres de contrôle de compte d’utilisateur (UAC) peuvent être affectés par stratégie de groupe paramètres sur les éditions Windows 7 professionnel, entreprise et édition intégrale, à l’instar de Windows Vista. Pour plus d’informations, consultez **Quelles sont les différences entre les différentes éditions de Windows Vista ? Comment les impactent-ils sur mon application DirectX ?**

</dd> <dt>

<span id="Will_DirectX_10_be_available_for_Windows_XP__"></span><span id="will_directx_10_be_available_for_windows_xp__"></span><span id="WILL_DIRECTX_10_BE_AVAILABLE_FOR_WINDOWS_XP__"></span>**DirectX 10 sera-t-il disponible pour Windows XP ?** 
</dt> <dd>

Non. Windows Vista, qui a DirectX 10, inclut un runtime DirectX mis à jour basé sur le runtime de Windows XP SP2 (DirectX 9.0 c) avec des modifications pour fonctionner avec le nouveau modèle WDDM (Windows Display Driver Model) et la nouvelle pile de pilotes audio, ainsi qu’avec d’autres mises à jour dans le système d’exploitation. En plus de Direct3D 9, Windows Vista prend en charge deux nouvelles interfaces lorsque le matériel et les pilotes vidéo corrects sont présents : Direct3D9Ex et Direct3D10.

Étant donné que ces nouvelles interfaces s’appuient sur la technologie WDDM, elles ne seront jamais disponibles sur les versions antérieures de Windows. Toutes les autres modifications apportées aux technologies DirectX pour Windows Vista sont également spécifiques à la nouvelle version de Windows. Le nom DirectX 10 trompe dans le fait que de nombreuses technologies fournies dans le kit de développement logiciel (SDK) DirectX (XACT, XINPUT, D3DX) ne sont pas comprises dans ce numéro de version. Ainsi, le fait de faire référence au numéro de version du runtime DirectX dans son ensemble a perdu une grande partie de sa signification, même pour la version 9.0 c. L’outil de diagnostic DirectX (DXdiag.exe) sur Windows Vista signale DirectX 10, mais cela fait uniquement référence à Direct3D 10.

</dd> <dt>

<span id="Will_DirectX_11_be_available_for_Windows_Vista_or_Windows_XP__"></span><span id="will_directx_11_be_available_for_windows_vista_or_windows_xp__"></span><span id="WILL_DIRECTX_11_BE_AVAILABLE_FOR_WINDOWS_VISTA_OR_WINDOWS_XP__"></span>**DirectX 11 sera-t-il disponible pour Windows Vista ou Windows XP ?** 
</dt> <dd>

DirectX 11 est intégré à Windows 7 et est disponible en tant que mise à jour pour Windows Vista (consultez <https://go.microsoft.com/fwlink/p/?linkid=160189> ). Cela comprend l’API Direct3D 11, l’infrastructure DirectX Graphics (DXGI) 1,1, les niveaux de fonctionnalités 10Level9, le périphérique de rendu logiciel de la plateforme Windows Advanced rastérisation (WARP) 10, Direct2D, DirectWrite et une mise à jour de l’API Direct3D 10,1 pour prendre en charge 10Level9 et WARP 10.

Pour les mêmes raisons que celles indiquées dans la question précédente (DirectX 10 sera-t-il **disponible pour Windows XP) ?** ), Direct3D 11 et les API associées ne sont pas disponibles sur Windows XP.

</dd> <dt>

<span id="What_Happened_to_DirectShow__I_can_t_find_it_in_the_DirectX_SDK._"></span><span id="what_happened_to_directshow__i_can_t_find_it_in_the_directx_sdk._"></span><span id="WHAT_HAPPENED_TO_DIRECTSHOW__I_CAN_T_FIND_IT_IN_THE_DIRECTX_SDK._"></span>**Qu’est-il arrivé à DirectShow ? Je ne le trouve pas dans le kit de développement logiciel (SDK) DirectX.** 
</dt> <dd>

DirectShow a été supprimé du kit de développement logiciel (SDK) DirectX à compter du 2005 avril. Vous pouvez obtenir les en-têtes, les bibliothèques, les outils et les exemples pour DirectShow dans le kit de développement logiciel (SDK) Windows (anciennement appelé Platform SDK). DirectSetup dans le kit de développement logiciel (SDK) DirectX continue à prendre en charge la redistribution des composants système de DirectShow, et les derniers composants sont déjà installés sur les systèmes d’exploitation suivants : Microsoft Windows XP Service Pack 2, Windows XP Professionnel Édition x64, Windows Server 2003 Service Pack 1 et Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_Vista__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_vista__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_VISTA__"></span>**Quelles modifications ont été apportées au runtime DirectX pour Windows Vista ?** 
</dt> <dd>

Les principales modifications ont été apportées pour prendre en charge le nouveau WDDM. Pour plus d’informations sur le nouveau modèle de pilote, sur les impacts sur Direct3D 9 et sur les deux nouvelles interfaces graphiques, Direct3D 9Ex et Direct3D 10, consultez [API graphiques dans Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista). Les nouvelles API graphiques pour Windows 7 (Direct3D 11, Direct2D, DirectWrite, DXGI 1,1 et Direct3D 10.1) sont disponibles en tant que mise à jour pour Windows Vista (consultez <https://go.microsoft.com/fwlink/p/?linkid=160189> ).

Windows Vista Service Pack 1 comprend une version mise à jour du runtime DirectX. Cette mise à jour étend la prise en charge de Windows Vista pour inclure Direct3D 10,1, exposant de nouvelles fonctionnalités matérielles facultatives. (Tout le matériel capable de prendre en charge Direct3D 10,1 prend également entièrement en charge toutes les fonctionnalités de Direct3D 10.)

DirectSound a été mis à jour pour exposer les fonctionnalités de la nouvelle pile de pilotes audio Windows Vista, qui prend en charge les mémoires tampons logicielles multicanal. L’API mode mémorisé Direct3D a été complètement supprimée de Windows Vista. DirectPlay Voice a également été supprimé, ainsi que le programme d’assistance NAT de DirectPlay et l’interface utilisateur du mappeur d’action de DirectInput. La prise en charge des interfaces DirectX 7 et DirectX 8 pour Visual Basic 6,0 n’est pas disponible sur Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_7__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_7__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_7__"></span>**Quelles modifications ont été apportées au runtime DirectX pour Windows 7 ?** 
</dt> <dd>

Windows 7 inclut tous les composants d’exécution DirectX disponibles dans Windows Vista et ajoute Direct3D 11, DXGI 1,1, 10Level9 Feature levels, The WARP10 Software Device, Direct2D, DirectWrite et une mise à jour de Direct3D 10,1 pour prendre en charge 10Level9 et WARP10. Pour plus d’informations, consultez [API graphiques dans Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista).

Tous les autres composants sont identiques à Windows Vista, avec l’ajout de la prise en charge native de 64 bits (x64) pour l’API DirectMusic de base liée à l’horodateur MIDI. La couche de performances de DirectMusic reste déconseillée et n’est disponible que pour les applications 32 bits sur Windows 7 pour la compatibilité des applications. Notez que la prise en charge native 64 bits de DirectMusic n’est pas disponible sur Windows Vista.

</dd> <dt>

<span id="I_think_I_have_found_a_driver_bug__what_do_I_do__"></span><span id="i_think_i_have_found_a_driver_bug__what_do_i_do__"></span><span id="I_THINK_I_HAVE_FOUND_A_DRIVER_BUG__WHAT_DO_I_DO__"></span>**Je pense que j’ai trouvé un bogue de pilote, que dois-je faire ?** 
</dt> <dd>

Tout d’abord, assurez-vous que vous avez vérifié les résultats avec le rastériseur de référence. Vérifiez ensuite les résultats avec la dernière version certifiée WHQL du pilote IHV. Vous pouvez vérifier par programme l’État WHQL à l’aide de la méthode GetAdapterIdentifier () sur l’interface IDirect3D9 en passant l' \_ indicateur de niveau WHQL D3DENUM \_ .

</dd> <dt>

<span id="Why_do_I_get_so_many_error_messages_when_I_try_to_compile_the_samples__"></span><span id="why_do_i_get_so_many_error_messages_when_i_try_to_compile_the_samples__"></span><span id="WHY_DO_I_GET_SO_MANY_ERROR_MESSAGES_WHEN_I_TRY_TO_COMPILE_THE_SAMPLES__"></span>**Pourquoi est-ce que j’obtiens un grand nombre de messages d’erreur lorsque j’essaie de compiler les exemples ?** 
</dt> <dd>

Vous n’avez probablement pas défini correctement votre chemin d’accès include. De nombreux compilateurs, y compris Microsoft Visual C++, incluent une version antérieure du kit de développement logiciel (SDK). par conséquent, si votre chemin d’accès include recherche d’abord dans les répertoires Include standard du compilateur, vous obtiendrez des versions incorrectes des fichiers d’en-tête. Pour remédier à ce problème, assurez-vous que le chemin d’accès include et les chemins de bibliothèque sont définis pour rechercher d’abord les chemins d’accès de bibliothèque et d’inclusion Microsoft DirectX. Voir aussi le fichier dxreadme.txt dans le kit de développement logiciel (SDK). Si vous installez le kit de développement logiciel (SDK) DirectX et que vous utilisez Visual C++, le programme d’installation peut éventuellement configurer les chemins d’accès include pour vous.

</dd> <dt>

<span id="I_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__GUIDs___what_do_I_do__"></span><span id="i_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__guids___what_do_i_do__"></span><span id="I_GET_LINKER_ERRORS_ABOUT_MULTIPLE_OR_MISSING_SYMBOLS_FOR_GLOBALLY_UNIQUE_IDENTIFIERS__GUIDS___WHAT_DO_I_DO__"></span>**J’obtiens des erreurs de l’éditeur de liens sur les symboles multiples ou manquants pour les identificateurs globaux uniques (GUID), que dois-je faire ?** 
</dt> <dd>

Les différents GUID que vous utilisez doivent être définis une fois et une seule. La définition du GUID est insérée si vous \# Définissez le symbole INITGUID avant d’inclure les fichiers d’en-tête DirectX. Par conséquent, vous devez vous assurer que cela se produit uniquement pour une unité de compilation. Une alternative à cette méthode consiste à établir une liaison avec la bibliothèque dxguid. lib, qui contient les définitions de tous les GUID DirectX. Si vous utilisez cette méthode (ce qui est recommandé), vous ne devez jamais \# définir le symbole INITGUID.

</dd> <dt>

<span id="Can_I_cast_a_pointer_to_a_DirectX_interface_to_a_lower_version_number__"></span><span id="can_i_cast_a_pointer_to_a_directx_interface_to_a_lower_version_number__"></span><span id="CAN_I_CAST_A_POINTER_TO_A_DIRECTX_INTERFACE_TO_A_LOWER_VERSION_NUMBER__"></span>**Puis-je effectuer un cast d’un pointeur vers une interface DirectX vers un numéro de version inférieur ?** 
</dt> <dd>

Non. Les interfaces DirectX sont des interfaces COM. Cela signifie qu’il n’y a aucune exigence pour que les interfaces numérotées les plus élevées soient dérivées des plus basses numérotées correspondantes. Par conséquent, le seul moyen sûr d’obtenir une interface différente pour un objet DirectX consiste à utiliser la méthode QueryInterface de l’interface. Cette méthode fait partie de l’interface IUnknown standard, à partir de laquelle toutes les interfaces COM doivent dériver.

</dd> <dt>

<span id="Can_I_mix_the_use_of_DirectX_9_components_and_DirectX_8_or_earlier_components_within_the_same_application__"></span><span id="can_i_mix_the_use_of_directx_9_components_and_directx_8_or_earlier_components_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECTX_9_COMPONENTS_AND_DIRECTX_8_OR_EARLIER_COMPONENTS_WITHIN_THE_SAME_APPLICATION__"></span>**Puis-je mélanger l’utilisation des composants DirectX 9 et DirectX 8 ou des composants antérieurs au sein de la même application ?** 
</dt> <dd>

Vous pouvez combiner librement différents composants de version différente ; par exemple, vous pouvez utiliser DirectInput 8 avec Direct3D 9 dans la même application. Toutefois, vous ne pouvez généralement pas mélanger différentes versions du même composant dans la même application ; par exemple, vous ne pouvez pas mélanger DirectDraw 7 avec Direct3D 9 (étant donné qu’il s’agit du même composant que DirectDraw, qui a été intégré à Direct3D depuis DirectX 8). Toutefois, il existe des exceptions, telles que l’utilisation de Direct3D 9 et de Direct3D 10 dans la même application, ce qui est autorisé.

</dd> <dt>

<span id="Can_I_mix_the_use_of_Direct3D_9_and_Direct3D_10_within_the_same_application__"></span><span id="can_i_mix_the_use_of_direct3d_9_and_direct3d_10_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECT3D_9_AND_DIRECT3D_10_WITHIN_THE_SAME_APPLICATION__"></span>**Puis-je mélanger l’utilisation de Direct3D 9 et de Direct3D 10 dans la même application ?** 
</dt> <dd>

Oui, vous pouvez utiliser ces versions de Direct3D ensemble dans la même application.

</dd> <dt>

<span id="What_do_the_return_values_from_the_Release_or_AddRef_methods_mean__"></span><span id="what_do_the_return_values_from_the_release_or_addref_methods_mean__"></span><span id="WHAT_DO_THE_RETURN_VALUES_FROM_THE_RELEASE_OR_ADDREF_METHODS_MEAN__"></span>**Que signifient les valeurs de retour des méthodes Release ou AddRef ?** 
</dt> <dd>

La valeur de retour sera le décompte de références actuel de l’objet. Toutefois, la spécification COM stipule que vous ne devez pas vous appuyer sur cela et la valeur est en général uniquement disponible à des fins de débogage. Les valeurs que vous observez peuvent être inattendues, car divers autres objets système peuvent contenir des références aux objets DirectX que vous créez. Pour cette raison, vous ne devez pas écrire de code qui appelle à plusieurs reprises la version jusqu’à ce que le nombre de références soit égal à zéro, car l’objet peut ensuite être libéré même si un autre composant peut encore y faire référence.

</dd> <dt>

<span id="Does_it_matter_in_which_order_I_release_DirectX_interfaces__"></span><span id="does_it_matter_in_which_order_i_release_directx_interfaces__"></span><span id="DOES_IT_MATTER_IN_WHICH_ORDER_I_RELEASE_DIRECTX_INTERFACES__"></span>**L’ordre dans lequel je libère les interfaces DirectX est-il important ?** 
</dt> <dd>

Cela ne devrait pas avoir d’importance, car les interfaces COM sont décomptées. Toutefois, il existe des bogues connus avec l’ordre de publication des interfaces dans certaines versions de DirectX. Pour des raisons de sécurité, il est recommandé de libérer des interfaces dans l’ordre de création inverse si possible.

</dd> <dt>

<span id="What_is_a_smart_pointer_and_should_I_use_it__"></span><span id="what_is_a_smart_pointer_and_should_i_use_it__"></span><span id="WHAT_IS_A_SMART_POINTER_AND_SHOULD_I_USE_IT__"></span>**Qu’est-ce qu’un pointeur intelligent et dois-je l’utiliser ?** 
</dt> <dd>

Un pointeur intelligent est une classe de modèle C++ conçue pour encapsuler les fonctionnalités de pointeur. En particulier, il existe des classes de pointeur intelligent standard conçues pour encapsuler des pointeurs d’interface COM. Ces pointeurs exécutent automatiquement QueryInterface au lieu d’un cast et ils gèrent AddRef et Release pour vous. La nécessité de les utiliser est en grande partie un goût. Si votre code contient un grand nombre de copies de pointeurs d’interface, avec plusieurs AddRefs et mises en production, les pointeurs intelligents peuvent probablement rendre votre code plus clair et réduire le risque d’erreur. Dans le cas contraire, vous ne pouvez pas les utiliser. Visual C++ comprend un pointeur intelligent Microsoft COM standard, défini dans le fichier d’en-tête « ComDef. h » (recherchez com \_ ptr \_ t dans l’aide).

</dd> <dt>

<span id="I_have_trouble_debugging_my_DirectX_application__any_tips__"></span><span id="i_have_trouble_debugging_my_directx_application__any_tips__"></span><span id="I_HAVE_TROUBLE_DEBUGGING_MY_DIRECTX_APPLICATION__ANY_TIPS__"></span>**Je ne parviens pas à déboguer mon application DirectX, quels sont les conseils ?** 
</dt> <dd>

Le problème le plus courant lors du débogage d’applications DirectX est la tentative de débogage alors qu’une surface DirectDraw est verrouillée. Cette situation peut provoquer un « verrou Win16 » sur les systèmes Microsoft Windows 9x, ce qui empêche la fenêtre du débogueur de se peindre. La spécification de l' \_ indicateur D3DLOCK NOSYSLOCK lors du verrouillage de la surface peut généralement éliminer cela. Windows 2000 ne souffre pas de ce problème. Lors du développement d’une application, il est utile de l’exécuter avec la version de débogage du runtime DirectX (sélectionnée quand vous installez le kit de développement logiciel (SDK)), qui effectue une validation de paramètre et génère des messages utiles à la sortie du débogueur.

</dd> <dt>

<span id="What_s_the_correct_way_to_check_return_codes__"></span><span id="what_s_the_correct_way_to_check_return_codes__"></span><span id="WHAT_S_THE_CORRECT_WAY_TO_CHECK_RETURN_CODES__"></span>**Quelle est la méthode correcte pour vérifier les codes de retour ?** 
</dt> <dd>

Utilisez les macros ayant réussi et échoué. Les méthodes DirectX peuvent retourner plusieurs codes de réussite et d’échec, donc un simple :

``` syntax
== D3D_OK
```

ou un test similaire ne suffira pas toujours.

</dd> <dt>

<span id="How_do_I_disable_ALT_TAB_and_other_task_switching__"></span><span id="how_do_i_disable_alt_tab_and_other_task_switching__"></span><span id="HOW_DO_I_DISABLE_ALT_TAB_AND_OTHER_TASK_SWITCHING__"></span>**Comment faire désactiver ALT + TAB et autres basculements de tâches ?** 
</dt> <dd>

Vous n’en avez pas ! Les jeux doivent être en mesure de gérer le basculement des tâches de manière appropriée, car de nombreux éléments peuvent se produire : ALT + TAB, connexions Bureau à distance, changement rapide d’utilisateur, limites d’utilisation des contrôles parentaux et beaucoup d’autres événements.

En même temps, deux sources courantes de basculement de tâche accidentel sur les jeux avec des schémas de contrôle centrés sur le clavier sont en appuyant sur la touche de logo Windows et en activant la fonction d’accessibilité touches rémanentes avec la touche Maj. Pour résoudre ces cas en désactivant les fonctionnalités, consultez les techniques décrites dans [désactivation des touches de raccourci dans les jeux](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Is_there_a_recommended_book_explaining_COM__"></span><span id="is_there_a_recommended_book_explaining_com__"></span><span id="IS_THERE_A_RECOMMENDED_BOOK_EXPLAINING_COM__"></span>**Existe-t-il un livre recommandé expliquant COM ?** 
</dt> <dd>

*Dans com* , Dale rogerson’s, publié par Microsoft Press, est une excellente introduction à com. Pour plus d’informations sur COM, nous vous recommandons vivement de consulter la boîte de Longman de l’ouvrage *Essential com* de don, publiée par.

</dd> <dt>

<span id="What_is_managed_code__"></span><span id="what_is_managed_code__"></span><span id="WHAT_IS_MANAGED_CODE__"></span>**Qu’est-ce que le code managé ?** 
</dt> <dd>

Le code managé est du code dont l’exécution est gérée par le .NET Framework CLR (Common Language Runtime). Il se rapporte à un contrat de collaboration entre le code d’exécution en mode natif et le Runtime. Ce contrat spécifie que, à tout moment de l’exécution, le runtime peut arrêter l’exécution d’un processeur et récupérer des informations spécifiques à l’adresse d’instruction de l’UC actuelle. Les informations qui doivent être en fonction des requêtes sont généralement liées à l’état d’exécution, telles que le contenu de la mémoire de l’enregistrement ou de la pile.

Avant l’exécution du code, le langage intermédiaire est compilé en code exécutable natif. Et, dans la mesure où cette compilation est effectuée par l’environnement d’exécution managé (ou, de manière plus correcte, par un compilateur qui sait comment cibler l’environnement d’exécution managé), l’environnement d’exécution managé peut apporter des garanties sur ce que le code va faire. Il peut insérer des interruptions et des raccordements de garbage collection appropriés, la gestion des exceptions, la sécurité de type, les limites de tableau et la vérification d’index, etc. Par exemple, un tel compilateur veille à disposer les frames de pile et tout ce qui est juste pour que le garbage collector puisse s’exécuter en arrière-plan sur un thread séparé, en continuant à parcourir la pile des appels active, en recherchant toutes les racines et en découvrant tous les objets actifs. En outre, étant donné que le langage intermédiaire a une notion de sécurité de type, le moteur d’exécution maintient la garantie de la sécurité de type en éliminant toute une classe d’erreurs de programmation qui mènent souvent à des brèches de sécurité.

En revanche, ce n’est pas le monde non géré : les fichiers exécutables non managés sont fondamentalement une image binaire, le code x86, chargée en mémoire. Le compteur de programme est placé là et c’est le dernier système d’exploitation qui le sait. Il existe des protections en place autour de la gestion de la mémoire et des e/s de port, etc., mais le système ne connaît pas réellement ce que fait l’application. Par conséquent, il ne peut apporter aucune garantie quant à ce qui se passe lorsque l’application s’exécute.

</dd> <dt>

<span id="What_books_are_there_about_general_Windows_programming__"></span><span id="what_books_are_there_about_general_windows_programming__"></span><span id="WHAT_BOOKS_ARE_THERE_ABOUT_GENERAL_WINDOWS_PROGRAMMING__"></span>**Quels sont les livres relatifs à la programmation Windows générale ?** 
</dt> <dd>

Paquet. Toutefois, les deux recommandations sont les suivantes :

-   Programmation de Windows par Charles Petzold (Microsoft Press)
-   Programmation d’applications pour Windows par Jeffrey Richter (Microsoft Press)

</dd> <dt>

<span id="How_do_I_debug_using_the_Windows_symbol_files__"></span><span id="how_do_i_debug_using_the_windows_symbol_files__"></span><span id="HOW_DO_I_DEBUG_USING_THE_WINDOWS_SYMBOL_FILES__"></span>**Comment faire déboguer à l’aide des fichiers de symboles Windows ?** 
</dt> <dd>

Microsoft publie des symboles supprimés pour toutes les DLL système (plus quelques autres). Pour y accéder, ajoutez ce qui suit à votre chemin d’accès aux symboles dans les paramètres du projet dans Visual Studio :

``` syntax
srv*https://msdl.microsoft.com/download/symbols
```

pour mettre en cache des symboles localement, utilisez la syntaxe suivante :

``` syntax
srv*c:\cache*https://msdl.microsoft.com/download/symbols
```

Où c : \\ cache est un répertoire local pour la mise en cache des fichiers de symboles.

</dd> </dl>

## <a name="direct3d-questions"></a>Questions sur Direct3D

### <a name="general-direct3d-questions"></a>Questions générales sur Direct3D

<dl> <dt>

<span id="Where_can_I_find_information_about_3D_graphics_techniques__"></span><span id="where_can_i_find_information_about_3d_graphics_techniques__"></span><span id="WHERE_CAN_I_FIND_INFORMATION_ABOUT_3D_GRAPHICS_TECHNIQUES__"></span>**Où puis-je trouver des informations sur les techniques graphiques 3D ?** 
</dt> <dd>

Le livre standard sur le sujet est Graphical Computer : principes et pratiques par Foley, Van Dam et al. Il s’agit d’une ressource précieuse pour toute personne souhaitant comprendre les fondements mathématiques des techniques de géométrie, de pixellisation et d’éclairage. Le Forum aux questions sur le groupe Usenet comp. Graphics. algorithmes contient également des informations utiles.

</dd> <dt>

<span id="Does_Direct3D_emulate_functionality_not_provided_by_hardware__"></span><span id="does_direct3d_emulate_functionality_not_provided_by_hardware__"></span><span id="DOES_DIRECT3D_EMULATE_FUNCTIONALITY_NOT_PROVIDED_BY_HARDWARE__"></span>**Direct3D émule-t-il des fonctionnalités non fournies par le matériel ?** 
</dt> <dd>

Cela dépend. Direct3D dispose d’un pipeline de traitement de vertex logiciel complet (y compris la prise en charge des nuanceurs de vertex personnalisés). Toutefois, aucune émulation n’est fournie pour les opérations de niveau pixel ; les applications doivent vérifier les bits de Cap appropriés et utiliser l’API ValidateDevice pour déterminer la prise en charge.

</dd> <dt>

<span id="Is_there_a_software_rasterizer_included_with_Direct3D__"></span><span id="is_there_a_software_rasterizer_included_with_direct3d__"></span><span id="IS_THERE_A_SOFTWARE_RASTERIZER_INCLUDED_WITH_DIRECT3D__"></span>**Un rastériseur logiciel est-il inclus avec Direct3D ?** 
</dt> <dd>

Pas pour les applications de performances. Un rastériseur de référence est fourni pour la validation du pilote, mais l’implémentation est conçue à des fins de précision et non de performances. Direct3D prend en charge les rastériseurs logiciels de plug-in.

</dd> <dt>

<span id="How_can_I_perform_color_keying_with_DirectX_graphics__"></span><span id="how_can_i_perform_color_keying_with_directx_graphics__"></span><span id="HOW_CAN_I_PERFORM_COLOR_KEYING_WITH_DIRECTX_GRAPHICS__"></span>**Comment puis-je effectuer une incrustation des couleurs avec DirectX Graphics ?** 
</dt> <dd>

Le masquage des couleurs n’est pas directement pris en charge, mais vous devez utiliser la fusion alpha pour émuler la clé de couleur. La fonction D3DXCreateTextureFromFileEx () peut être utilisée pour faciliter cette tâche. Cette fonction accepte un paramètre de couleur de clé et remplace tous les pixels de l’image source contenant la couleur spécifiée par des pixels noirs transparents dans la texture créée.

</dd> <dt>

<span id="Does_the_Direct3D_geometry_code_utilize_3DNow__and_or_Pentium_III_SIMD_instructions__"></span><span id="does_the_direct3d_geometry_code_utilize_3dnow__and_or_pentium_iii_simd_instructions__"></span><span id="DOES_THE_DIRECT3D_GEOMETRY_CODE_UTILIZE_3DNOW__AND_OR_PENTIUM_III_SIMD_INSTRUCTIONS__"></span>**Le code de géométrie Direct3D utilise-t-il des instructions 3DNow ! et/ou Pentium III SIMD ?** 
</dt> <dd>

Oui. Le pipeline de géométrie Direct3D a plusieurs chemins de code différents, en fonction du type de processeur, et il utilisera les opérations à virgule flottante spéciales fournies par le processeur 3DNow ! ou les instructions Pentium III SIMD où elles sont disponibles. Cela comprend le traitement des nuanceurs de vertex personnalisés.

</dd> <dt>

<span id="How_do_I_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="how_do_i_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="HOW_DO_I_PREVENT_TRANSPARENT_PIXELS_BEING_WRITTEN_TO_THE_Z-BUFFER__"></span>**Comment faire empêcher les pixels transparents écrits dans la mémoire tampon z ?** 
</dt> <dd>

Vous pouvez filtrer les pixels avec une valeur alpha au-dessus ou en dessous d’un seuil donné. Vous contrôlez ce comportement à l’aide de renderstates ALPHATESTENABLE, ALPHAREF et ALPHAFUNC.

</dd> <dt>

<span id="What_is_a_stencil_buffer__"></span><span id="what_is_a_stencil_buffer__"></span><span id="WHAT_IS_A_STENCIL_BUFFER__"></span>**Qu’est-ce qu’une mémoire tampon de stencil ?** 
</dt> <dd>

Une mémoire tampon de stencil est une mémoire tampon supplémentaire d’informations par pixel, similaire à une mémoire tampon z. En fait, elle réside dans certains bits d’une mémoire tampon z. Les formats courants stencil/z-buffer sont les modèles z et 1-bit 15 bits, ou le gabarit z et 8 bits de 24 bits. Il est possible d’effectuer des opérations arithmétiques simples sur le contenu de la mémoire tampon de stencil, en fonction du pixel, lors du rendu des polygones. Par exemple, la mémoire tampon de stencil peut être incrémentée ou décrémentée, ou le pixel peut être rejeté si la valeur du stencil échoue à un test de comparaison simple. Cela est utile pour les effets qui impliquent le marquage d’une région de la mémoire tampon de trame, puis le rendu uniquement de la région marquée (ou non marquée). De bons exemples sont des effets volumétriques comme les volumes de clichés instantanés.

</dd> <dt>

<span id="How_do_I_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="how_do_i_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="HOW_DO_I_USE_A_STENCIL_BUFFER_TO_RENDER_SHADOW_VOLUMES__"></span>**Comment faire utiliser une mémoire tampon de stencil pour restituer les volumes de clichés instantanés ?** 
</dt> <dd>

La clé de cet et d’autres effets de tampon de stencils volumétriques est l’interaction entre la mémoire tampon de stencil et la mémoire tampon z. Une scène avec un volume de cliché instantané est rendue en trois étapes. Tout d’abord, la scène sans ombre est rendue comme d’habitude, à l’aide de la mémoire tampon z. Ensuite, l’ombre est indiquée dans la mémoire tampon du stencil comme suit. Les faces avant du volume de cliché instantané sont dessinées à l’aide de polygones invisibles, le test z étant activé, mais les écritures z sont désactivées et la mémoire tampon du stencil s’incrémente à chaque pixel passant le test z. Les faces arrière du volume de cliché instantané sont rendues de la même façon, mais en décrémentant la valeur du stencil à la place.

À présent, envisagez un seul pixel. En supposant que l’appareil photo n’est pas dans le volume de cliché instantané, il y a quatre possibilités pour le point correspondant dans la scène. Si le rayon de l’appareil photo vers le point n’interfère pas avec le volume de cliché instantané, aucun polygone d’ombre n’aura été dessiné à cet endroit et la mémoire tampon du stencil est toujours égale à zéro. Dans le cas contraire, si le point se trouve devant le volume de cliché instantané, les polygones de l’ombre sont mis en mémoire tampon z et le gabarit reste inchangé. Si les points se trouvent derrière le volume de cliché instantané, le même nombre de faces d’ombre avant que les faces arrière auront été rendues et le stencil sera égal à zéro, ayant été incrémenté autant de fois que le nombre de fois décrémenté.

La dernière possibilité est que le point se trouve à l’intérieur du volume de cliché instantané. Dans ce cas, la face arrière du volume de cliché instantané est z-mise en mémoire tampon, mais pas la face avant, donc la mémoire tampon du stencil est une valeur différente de zéro. Le résultat est une partie de la mémoire tampon de trame située dans l’ombre a une valeur de stencil différente de zéro. Enfin, pour restituer réellement l’ombre, l’ensemble de la scène est lavé avec un polygone à contrôle alpha défini pour affecter uniquement les pixels avec une valeur de stencil différente de zéro. Vous pouvez voir un exemple de cette technique dans l’exemple « volume de cliché instantané » fourni avec le kit de développement logiciel (SDK) DirectX.

</dd> <dt>

<span id="What_are_the_texel_alignment_rules__How_do_I_get_a_one-to-one_mapping__"></span><span id="what_are_the_texel_alignment_rules__how_do_i_get_a_one-to-one_mapping__"></span><span id="WHAT_ARE_THE_TEXEL_ALIGNMENT_RULES__HOW_DO_I_GET_A_ONE-TO-ONE_MAPPING__"></span>**Quelles sont les règles d’alignement de Texel ? Comment faire obtenir un mappage un-à-un ?** 
</dt> <dd>

Cette procédure est entièrement expliquée dans la documentation de Direct3D 9. Toutefois, le résumé est que vous devez biaiser vos coordonnées d’écran par-0,5 d’un pixel afin de les aligner correctement avec les texels. La plupart des cartes se conforment désormais correctement aux règles d’alignement de Texel, mais il existe des cartes ou des pilotes plus anciens qui ne le sont pas. Pour gérer ces cas-là, nous vous recommandons de contacter le fournisseur de matériel en question et de demander des pilotes mis à jour ou leur solution de contournement suggérée. Notez que dans Direct3D 10, cette règle ne contient plus.

</dd> <dt>

<span id="What_is_the_purpose_of_the_D3DCREATE_PUREDEVICE_flag__"></span><span id="what_is_the_purpose_of_the_d3dcreate_puredevice_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_D3DCREATE_PUREDEVICE_FLAG__"></span>**Quel est l’objectif de l' \_ indicateur D3DCREATE PUREDEVICE ?** 
</dt> <dd>

Utilisez l' \_ indicateur D3DCREATE PUREDEVICE lors de la création de l’appareil pour créer un appareil pur. Un appareil pur n’enregistre pas l’état actuel (lors des modifications d’État), ce qui améliore souvent les performances. Cet appareil nécessite également le traitement du vertex matériel. Un appareil pur est généralement utilisé lorsque le développement et le débogage sont terminés, et que vous souhaitez obtenir des performances optimales.

L’un des inconvénients d’un appareil pur est qu’il ne prend pas en charge tous les appels d’API d’extraction \* . cela signifie que vous ne pouvez pas utiliser un appareil pur pour interroger l’état du pipeline. Cela complique le débogage lors de l’exécution d’une application. Vous trouverez ci-dessous une liste de toutes les méthodes qui sont désactivées par un appareil pur.

-   [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane)
-   [**IDirect3DDevice9::GetClipStatus**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipstatus)
-   [**IDirect3DDevice9::GetLight**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight)
-   [**IDirect3DDevice9::GetLightEnable**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable)
-   [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial)
-   [**IDirect3DDevice9::GetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf)
-   [**IDirect3DDevice9::GetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti)
-   [**IDirect3DDevice9::GetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb)
-   [**IDirect3DDevice9::GetRenderState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrenderstate)
-   [**IDirect3DDevice9::GetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate)
-   [**IDirect3DDevice9::GetTextureStageState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate)
-   [**IDirect3DDevice9::GetTransform**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform)
-   [**IDirect3DDevice9::GetVertexShaderConstantF**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantf)
-   [**IDirect3DDevice9::GetVertexShaderConstantI**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstanti)
-   [**IDirect3DDevice9::GetVertexShaderConstantB**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantb)

Le deuxième inconvénient d’un appareil pur est qu’il ne filtre pas les modifications d’État redondantes. Lorsque vous utilisez un appareil pur, votre application doit réduire au minimum le nombre de modifications d’État dans la boucle de rendu ; Cela peut inclure le filtrage des modifications d’État pour s’assurer que les États ne sont pas définis plusieurs fois. Ce compromis dépend de l’application ; Si vous utilisez plus d’un 1000 appels d’ensemble par trame, vous devez envisager de tirer parti du filtrage de redondance effectué automatiquement par un appareil non pur.

Comme pour tous les problèmes de performances, le seul moyen de savoir si votre application fonctionnera mieux avec un appareil pur est de comparer les performances de votre application à un appareil pur ou non pur. Un appareil pur a le potentiel d’accélérer une application en réduisant la charge de l’UC de l’API. Soyez prudent ! Dans certains scénarios, un appareil pur ralentit votre application (en raison du travail supplémentaire du processeur provoqué par les changements d’État redondants). Si vous ne savez pas quel type d’appareil fonctionne le mieux pour votre application et que vous ne filtrez pas les modifications redondantes dans l’application, utilisez un appareil non pur.

</dd> <dt>

<span id="How_do_I_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="how_do_i_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="HOW_DO_I_ENUMERATE_THE_DISPLAY_DEVICES_IN_A_MULTI-MONITOR_SYSTEM__"></span>**Comment faire énumérer les appareils d’affichage dans un système à plusieurs écrans ?** 
</dt> <dd>

L’énumération peut être effectuée par le biais d’une itération simple par l’application à l’aide de méthodes de l’interface IDirect3D9. Appelez GetAdapterCount pour déterminer le nombre d’adaptateurs d’affichage dans le système. Appelez GetAdapterMonitor pour déterminer à quel moniteur physique une carte est connectée (cette méthode retourne un HMONITOR, que vous pouvez ensuite utiliser dans le GetMonitorInfo de l’API Win32 pour déterminer les informations relatives au moniteur physique). La détermination des caractéristiques d’un adaptateur d’affichage particulier ou la création d’un périphérique Direct3D sur cet adaptateur est aussi simple que la transmission du numéro d’adaptateur approprié à la place de D3DADAPTER \_ par défaut lors de l’appel de GetDeviceCaps, CreateDevice ou d’autres méthodes.

</dd> <dt>

<span id="What_happened_to_Fixed_Function_Bumpmapping_in_D3D9__"></span><span id="what_happened_to_fixed_function_bumpmapping_in_d3d9__"></span><span id="WHAT_HAPPENED_TO_FIXED_FUNCTION_BUMPMAPPING_IN_D3D9__"></span>**Qu’est-il arrivé à la fonction Fixed Bumpmapping dans D3D9 ?** 
</dt> <dd>

À compter de Direct3D 9, nous avons renforcé la validation sur les cartes qui pouvaient uniquement prendre en charge > 2 textures simultanées. Certaines anciennes cartes ne disposent que de 3 étapes de texture disponibles lorsque vous utilisez une opération de modulation alpha spécifique. L’utilisation la plus courante que les utilisateurs utilisent en 3 étapes pour est emboss bumpmapping, et vous pouvez toujours le faire avec D3D9.

Le champ Height doit être stocké dans le canal alpha et utilisé pour moduler la contribution de l’éclairage, c’est-à-dire :

``` syntax
// Stage 0 is the base texture, with the height map in the alpha channel
m_pd3dDevice->SetTexture(0, m_pEmbossTexture );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 0 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP,   D3DTOP_MODULATE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP,   D3DTOP_SELECTARG1 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE );
if( m_bShowEmbossMethod )
{
 // Stage 1 passes through the RGB channels (SELECTARG2 = CURRENT), and 
 // does a signed add with the inverted alpha channel. 
 // The texture coords associated with Stage 1 are the shifted ones, so 
 // the result is:
 //    (height - shifted_height) * tex.RGB * diffuse.RGB
   m_pd3dDevice->SetTexture( 1, m_pEmbossTexture );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_SELECTARG2 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAOP, D3DTOP_ADDSIGNED );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG1, D3DTA_TEXTURE|D3DTA_COMPLEMENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG2, D3DTA_CURRENT );

   // Set up the alpha blender to multiply the alpha channel 
   // (monochrome emboss) with the src color (lighted texture)
   m_pd3dDevice->SetRenderState( D3DRS_ALPHABLENDENABLE, TRUE );
   m_pd3dDevice->SetRenderState( D3DRS_SRCBLEND,  D3DBLEND_SRCALPHA );
   m_pd3dDevice->SetRenderState( D3DRS_DESTBLEND, D3DBLEND_ZERO );
}
```

Cet exemple, avec d’autres exemples plus anciens, n’est plus fourni dans la version actuelle du kit de développement logiciel (SDK) et ne sera pas fourni dans les futures versions du SDK.

</dd> </dl>

### <a name="geometry-vertex-processing"></a>Traitement Geometry (vertex)

<dl> <dt>

<span id="Vertex_streams_confuse_me_how_do_they_work__"></span><span id="vertex_streams_confuse_me_how_do_they_work__"></span><span id="VERTEX_STREAMS_CONFUSE_ME_HOW_DO_THEY_WORK__"></span>**Les flux vertex embrouillent comment fonctionnent-ils ?** 
</dt> <dd>

Direct3D assemble chaque vertex qui est chargé dans la portion de traitement du pipeline à partir d’un ou de plusieurs flux de vertex. Le fait d’avoir un seul flux de vertex correspond à l’ancien modèle antérieur à DirectX 8, dans lequel les vertex proviennent d’une source unique. Avec DirectX 8, différents composants vertex peuvent provenir de différentes sources. par exemple, une mémoire tampon de vertex peut contenir des positions et des normales, tandis qu’une deuxième stocke des valeurs de couleur et des coordonnées de texture.

</dd> <dt>

<span id="What_is_a_vertex_shader__"></span><span id="what_is_a_vertex_shader__"></span><span id="WHAT_IS_A_VERTEX_SHADER__"></span>**Qu’est-ce qu’un nuanceur vertex ?** 
</dt> <dd>

Un nuanceur de sommets est une procédure de traitement d’un seul vertex. Il est défini à l’aide d’un langage simple de type assembly assemblé par la bibliothèque de l’utilitaire D3DX dans un flux de jetons accepté par Direct3D. Le nuanceur de sommets prend comme entrée un seul vertex et un ensemble de valeurs constantes ; elle génère une position de vertex (dans l’espace) et éventuellement un ensemble de couleurs et de coordonnées de texture, qui sont utilisées dans la pixellisation. Notez que lorsque vous disposez d’un nuanceur vertex personnalisé, les composants de vertex n’ont plus de sémantique appliquée par Direct3D et les vertex sont simplement des données arbitraires qui sont interprétées par le nuanceur de sommets que vous créez.

</dd> <dt>

<span id="Does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="DOES_A_VERTEX_SHADER_PERFORM_PERSPECTIVE_DIVISION_OR_CLIPPING__"></span>**Un nuanceur vertex effectue-t-il une division ou un découpage ?** 
</dt> <dd>

Non. Le nuanceur de sommets génère une coordonnée homogène dans l’espace pour la position du vertex transformé. La Division et le découpage de la perspective sont effectués automatiquement après le nuanceur.

</dd> <dt>

<span id="Can_I_generate_geometry_with_a_vertex_shader__"></span><span id="can_i_generate_geometry_with_a_vertex_shader__"></span><span id="CAN_I_GENERATE_GEOMETRY_WITH_A_VERTEX_SHADER__"></span>**Puis-je générer une géométrie avec un nuanceur de sommets ?** 
</dt> <dd>

Un nuanceur de sommets ne peut pas créer ou détruire des vertex ; elle opère sur un seul vertex à la fois, en acceptant un vertex non traité comme entrée et en générant un vertex traité unique. Il peut donc être utilisé pour manipuler la géométrie existante (en appliquant des déformations ou en effectuant des opérations d’application d’apparence), mais ne peut pas générer une nouvelle géométrie par se.

</dd> <dt>

<span id="Can_I_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="can_i_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="CAN_I_APPLY_A_CUSTOM_VERTEX_SHADER_TO_THE_RESULTS_OF_THE_FIXED-FUNCTION_GEOMETRY_PIPELINE__OR_VICE-VERSA___"></span>**Puis-je Appliquer un nuanceur vertex personnalisé aux résultats du pipeline Geometry à fonction fixe (ou inversement) ?** 
</dt> <dd>

Non. Vous devez choisir l’un ou l’autre. Si vous utilisez un nuanceur de sommets personnalisé, vous êtes responsable de l’exécution de la transformation de vertex entière.

</dd> <dt>

<span id="Can_I_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="can_i_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="CAN_I_USE_A_CUSTOM_VERTEX_SHADER_IF_MY_HARDWARE_DOES_NOT_SUPPORT_IT__"></span>**Puis-je utiliser un nuanceur vertex personnalisé si mon matériel ne le prend pas en charge ?** 
</dt> <dd>

Oui. Le moteur de traitement des vertex du logiciel Direct3D prend entièrement en charge les nuanceurs vertex personnalisés avec un niveau étonnamment élevé de performances.

</dd> <dt>

<span id="How_do_I_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="how_do_i_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="HOW_DO_I_DETERMINE_IF_THE_HARDWARE_SUPPORTS_MY_CUSTOM_VERTEX_SHADER__"></span>**Comment faire déterminer si le matériel prend en charge mon nuanceur vertex personnalisé ?** 
</dt> <dd>

Les appareils qui peuvent prendre en charge des nuanceurs vertex dans le matériel sont requis pour remplir le champ D3DCAPS9 :: VertexShaderVersion pour indiquer le niveau de version du nuanceur de sommets qu’ils prennent en charge. Tout appareil revendiquant la prise en charge d’un niveau particulier de nuanceur vertex doit prendre en charge tous les nuanceurs de vertex légaux qui répondent à la spécification de ce niveau ou ci-dessous.

</dd> <dt>

<span id="How_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="how_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="HOW_MANY_CONSTANT_REGISTERS_ARE_AVAILABLE_FOR_VERTEX_SHADERS__"></span>**Combien de registres constants sont disponibles pour les nuanceurs vertex ?** 
</dt> <dd>

Les appareils prenant en charge les nuanceurs vertex vs 1,0 sont requis pour prendre en charge un minimum de 96 registres constants. Les appareils peuvent prendre en charge plus que ce nombre minimal et peuvent les signaler via le champ D3DCAPS9 :: MaxVertexShaderConst.

</dd> <dt>

<span id="Can_I_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="can_i_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="CAN_I_SHARE_POSITION_DATA_BETWEEN_VERTICES_WITH_DIFFERENT_TEXTURE_COORDINATES__"></span>**Puis-je partager des données de position entre des vertex avec des coordonnées de texture différentes ?** 
</dt> <dd>

L’exemple habituel de cette situation est un cube dans lequel vous souhaitez utiliser une texture différente pour chaque visage. Malheureusement, la réponse est non, il n’est pas actuellement possible d’indexer les composants de vertex indépendamment. Même avec plusieurs flux de vertex, tous les flux sont indexés ensemble.

</dd> <dt>

<span id="When_I_submit_an_indexed_list_of_primitives__does_Direct3D_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_I_indexed__"></span><span id="when_i_submit_an_indexed_list_of_primitives__does_direct3d_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_i_indexed__"></span><span id="WHEN_I_SUBMIT_AN_INDEXED_LIST_OF_PRIMITIVES__DOES_DIRECT3D_PROCESS_ALL_OF_THE_VERTICES_IN_THE_BUFFER__OR_JUST_THE_ONES_I_INDEXED__"></span>**Lorsque j’envoie une liste indexée de primitives, Direct3D traite-t-il tous les vertex dans la mémoire tampon, ou seulement ceux que j’ai indexés ?** 
</dt> <dd>

Lors de l’utilisation du pipeline de géométrie logicielle, Direct3D transforme tout d’abord tous les vertex de la plage que vous avez envoyée, plutôt que de les transformer « à la demande » à mesure qu’ils sont indexés. Pour les données compactées (c’est-à-dire, où la plupart des vertex sont utilisés), cette solution est plus efficace, en particulier lorsque des instructions SIMD sont disponibles. Si vos données sont peu compressées (c’est-à-dire que de nombreux vertex ne sont pas utilisés), vous pouvez envisager de réorganiser vos données afin d’éviter un trop grand nombre de transformations redondantes. Lors de l’utilisation de l’accélération de la géométrie matérielle, les vertex sont généralement transformés à la demande à mesure qu’ils sont requis.

</dd> <dt>

<span id="What_is_an_index_buffer__"></span><span id="what_is_an_index_buffer__"></span><span id="WHAT_IS_AN_INDEX_BUFFER__"></span>**Qu’est-ce qu’un tampon d’index ?** 
</dt> <dd>

Une mémoire tampon d’index est exactement analogue à une mémoire tampon de vertex, mais elle contient des index à utiliser dans les appels DrawIndexedPrimitive. Il est fortement recommandé d’utiliser des mémoires tampons d’index plutôt que de la mémoire allouée à l’application brute lorsque cela est possible, pour les mêmes raisons que les mémoires tampons de vertex.

</dd> <dt>

<span id="I_notice_that_32-bit_indices_are_a_supported_type__can_I_use_them_on_all_devices__"></span><span id="i_notice_that_32-bit_indices_are_a_supported_type__can_i_use_them_on_all_devices__"></span><span id="I_NOTICE_THAT_32-BIT_INDICES_ARE_A_SUPPORTED_TYPE__CAN_I_USE_THEM_ON_ALL_DEVICES__"></span>**Je remarque que les index 32 bits sont un type pris en charge ; puis-je les utiliser sur tous les appareils ?** 
</dt> <dd>

Non. Vous devez vérifier le champ D3DCAPS9 :: MaxVertexIndex pour déterminer la valeur d’index maximale prise en charge par l’appareil. Cette valeur doit être supérieure à 2 pour le 16ème-1 (0xFFFF) afin que les mémoires tampons d’index de type D3DFMT \_ INDEX32 soient prises en charge. Notez également que certains appareils peuvent prendre en charge les index 32 bits, mais prennent en charge une valeur d’index maximale inférieure à 2 pour 32e Power-1 (0xFFFFFFFF); dans ce cas, l’application doit respecter la limite indiquée par l’appareil.

</dd> <dt>

<span id="Does_S_W_vertex_processing_support_64_bit__"></span><span id="does_s_w_vertex_processing_support_64_bit__"></span><span id="DOES_S_W_VERTEX_PROCESSING_SUPPORT_64_BIT__"></span>**Le traitement des vertex S/W prend-il en charge 64 bits ?** 
</dt> <dd>

Il existe un pipeline de vertex s/w optimisé pour x64, mais il n’existe pas pour IA64.

</dd> </dl>

### <a name="performance-tuning"></a>Réglage des performances

<dl> <dt>

<span id="How_can_I_improve_the_performance_of_my_Direct3D_application__"></span><span id="how_can_i_improve_the_performance_of_my_direct3d_application__"></span><span id="HOW_CAN_I_IMPROVE_THE_PERFORMANCE_OF_MY_DIRECT3D_APPLICATION__"></span>**Comment améliorer les performances de mon application Direct3D ?** 
</dt> <dd>

Voici les principaux points à consulter lors de l’optimisation des performances :

<dl> <dt>

<span id="Batch_size_"></span><span id="batch_size_"></span><span id="BATCH_SIZE_"></span>**Taille du lot** 
</dt> <dd>

Direct3D est optimisé pour les grands lots de Primitives. Plus il y a de polygones qui peuvent être envoyés en un seul appel, mieux c’est. Une bonne règle empirique consiste à viser la moyenne de 1000 sommets par appel primitif. Au-dessous de ce niveau, vous n’obtiendrez probablement pas de performances optimales, au-dessus de cela et vous êtes en train de réduire les retours et les conflits potentiels avec les considérations d’accès concurrentiel (voir ci-dessous).

</dd> <dt>

<span id="State_changes_"></span><span id="state_changes_"></span><span id="STATE_CHANGES_"></span>**Modifications d’État** 
</dt> <dd>

La modification de l’état du rendu peut être une opération coûteuse, en particulier lors de la modification de la texture. Pour cette raison, il est important de réduire autant que possible le nombre de modifications d’État effectuées par image. Essayez également de réduire les modifications de la mémoire tampon de vertex ou d’index.

> [!Note]  
> Depuis DirectX 8, le coût du changement de mémoire tampon de vertex n’est plus aussi coûteux qu’avec les versions précédentes, mais il est toujours conseillé d’éviter les modifications de tampon de vertex lorsque cela est possible.

 

</dd> <dt>

<span id="Concurrency"></span><span id="concurrency"></span><span id="CONCURRENCY"></span>**D’accès concurrentiel**
</dt> <dd>

Si vous pouvez faire en sorte d’effectuer un rendu simultané avec un autre traitement, vous tirerez pleinement parti des performances du système. Cet objectif peut être en conflit avec l’objectif de la réduction des modifications apportées à RenderState. Vous devez trouver un juste équilibre entre le traitement par lot pour réduire les changements d’État et pousser les données vers le pilote tôt pour permettre l’accès concurrentiel. L’utilisation de plusieurs mémoires tampons de vertex en mode de tourniquet (Round Robin) peut faciliter la concurrence.

</dd> <dt>

<span id="Texture_uploads_"></span><span id="texture_uploads_"></span><span id="TEXTURE_UPLOADS_"></span>**Chargements de texture** 
</dt> <dd>

Le chargement de textures sur l’appareil consomme de la bande passante et entraîne une concurrence de bande passante avec les données de vertex. Par conséquent, il est important de ne pas dépasser la mémoire de texture de validation, ce qui force votre schéma de mise en cache à télécharger une quantité excessive de textures de chaque trame.

</dd> <dt>

<span id="Vertex_and_index_buffers_"></span><span id="vertex_and_index_buffers_"></span><span id="VERTEX_AND_INDEX_BUFFERS_"></span>**Mémoires tampons de vertex et d’index** 
</dt> <dd>

Vous devez toujours utiliser des mémoires tampons de vertex et d’index, plutôt que des blocs simples de mémoire allouée à l’application. Au minimum, la sémantique de verrouillage pour les mémoires tampons de vertex et d’index peut éviter une opération de copie redondante. Avec certains pilotes, le tampon de vertex ou d’index peut être placé dans une mémoire plus optimale (peut-être dans la mémoire vidéo ou AGP) pour que le matériel puisse y accéder.

</dd> <dt>

<span id="State_macro_blocks_"></span><span id="state_macro_blocks_"></span><span id="STATE_MACRO_BLOCKS_"></span>**Blocs de macros d’État** 
</dt> <dd>

Celles-ci ont été introduites dans DirectX 7,0. Ils fournissent un mécanisme d’enregistrement d’une série de modifications d’État (y compris des modifications d’éclairage, de matériau et de matrice) dans une macro, qui peut ensuite être relue par un appel unique. Ceci présente deux avantages :

-   Vous réduisez la charge des appels en effectuant un appel au lieu de plusieurs.
-   Un pilote sensible peut pré-analyser et précompiler les modifications d’État, ce qui le rend plus rapide à soumettre au matériel graphique.

Les modifications d’État peuvent toujours être onéreuses, mais l’utilisation de macros d’état permet de réduire au moins certains coûts. Utilisez un seul appareil Direct3D. Si vous devez effectuer le rendu sur plusieurs cibles, utilisez SetRenderTarget. Si vous créez une application avec fenêtres avec plusieurs fenêtres 3D, utilisez l’API CreateAdditionalSwapChain. Le runtime est optimisé pour un appareil unique et une baisse de la vitesse est considérable pour l’utilisation de plusieurs appareils.

</dd> </dl> </dd> <dt>

<span id="Which_primitive_types__strips__fans__lists_and_so_on__should_I_use__"></span><span id="which_primitive_types__strips__fans__lists_and_so_on__should_i_use__"></span><span id="WHICH_PRIMITIVE_TYPES__STRIPS__FANS__LISTS_AND_SO_ON__SHOULD_I_USE__"></span>**Quels types primitifs (bandes, fans, listes, etc.) dois-je utiliser ?** 
</dt> <dd>

De nombreux maillages ont été rencontrés dans des vertex de fonctionnalités de données réelles qui sont partagés par plusieurs polygones. Pour optimiser les performances, il est souhaitable de réduire la duplication des vertex transformés et envoyés sur le bus au périphérique de rendu. Il est clair que l’utilisation de simples listes de triangles ne permet pas de partager des vertex, ce qui en fait la méthode la moins optimale. Le choix consiste ensuite à utiliser des bandes et des ventilateurs, ce qui implique une relation de connectivité spécifique entre les polygones et l’utilisation de listes indexées. Lorsque les données se trouvent naturellement dans des barrettes et des ventilateurs, il s’agit du choix le plus approprié, car ils réduisent les données envoyées au pilote. Toutefois, la décomposition des mailles en barrettes et ventilateurs aboutit souvent à un grand nombre d’éléments séparés, impliquant un grand nombre d’appels DrawPrimitive. C’est la raison pour laquelle la méthode la plus efficace consiste généralement à utiliser un seul appel DrawIndexedPrimitive avec une liste de triangles. L’un des avantages supplémentaires de l’utilisation d’une liste indexée est qu’un avantage peut être obtenu même lorsque les triangles consécutifs partagent uniquement un seul vertex. En résumé, si vos données se trouvent naturellement dans de larges bandes ou ventilateurs, utilisez des bandes ou des ventilateurs. Sinon, utilisez des listes indexées.

</dd> <dt>

<span id="How_do_you_determine_the_total_texture_memory_a_card_has__excluding_AGP_memory__"></span><span id="how_do_you_determine_the_total_texture_memory_a_card_has__excluding_agp_memory__"></span><span id="HOW_DO_YOU_DETERMINE_THE_TOTAL_TEXTURE_MEMORY_A_CARD_HAS__EXCLUDING_AGP_MEMORY__"></span>**Comment déterminer la quantité totale de mémoire de texture d’une carte, à l’exclusion de la mémoire AGP ?** 
</dt> <dd>

[**IDirect3DDevice9 :: GetAvailableTextureMem**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getavailabletexturemem) retourne la mémoire totale disponible, y compris l’AGP. L’allocation de ressources en fonction de la quantité de mémoire vidéo que vous avez n’est pas une bonne idée. Par exemple, que se passe-t-il si la carte s’exécute sous une mémoire UMA (Unified Memory Architecture) ou est capable de compresser les textures ? Il peut y avoir plus d’espace disponible que prévu. Vous devez créer des ressources et vérifier les erreurs de mémoire insuffisante, puis redimensionner les textures. Par exemple, vous pouvez supprimer les principaux niveaux MIP de vos Textures.

</dd> <dt>

<span id="What_s_a_good_usage_pattern_for_vertex_buffers_if_I_m_generating_dynamic_data__"></span><span id="what_s_a_good_usage_pattern_for_vertex_buffers_if_i_m_generating_dynamic_data__"></span><span id="WHAT_S_A_GOOD_USAGE_PATTERN_FOR_VERTEX_BUFFERS_IF_I_M_GENERATING_DYNAMIC_DATA__"></span>**Quel est le modèle d’utilisation approprié pour les mémoires tampons de vertex si je génère des données dynamiques ?** 
</dt> <dd>

1.  Créez une mémoire tampon de vertex à l’aide des \_ indicateurs d’utilisation D3DUSAGE dynamique et D3DUSAGE \_ WRITEONLY et de l' \_ indicateur de pool par défaut D3DPOOL. (Spécifiez également D3DUSAGE \_ SOFTWAREPROCESSING si vous utilisez le traitement du vertex logiciel.)
2.  I = 0.
3.  Définissez State (textures, renderstates, etc.).
4.  Vérifiez s’il y a de l’espace dans la mémoire tampon, autrement dit, par exemple, I + M <= N ? (Où M est le nombre de nouveaux vertex).
5.  Si c’est le cas, verrouillez le VB avec D3DLOCK \_ NOOVERWRITE. Cela indique à Direct3D et au pilote que vous allez ajouter des vertex et ne modifie pas ceux que vous avez précédemment regroupés par lots. Par conséquent, si une opération DMA était en cours, elle n’est pas interrompue. Si ce n’est pas le cas, Goto 11.
6.  Renseignez les sommets M à I.
7.  Bloquer.
8.  Appelez une \[ primitive indexée \] . Pour les primitives non indexées, utilisez I comme paramètre StartVertex. Pour les primitives indexées, vérifiez que les index pointent vers la partie correcte de la mémoire tampon de vertex (il peut être plus facile d’utiliser le paramètre BaseVertexIndex de l’appel SetIndices pour y parvenir).
9.  I + = M.
10. Goto 3.
11. OK, nous n’avons pas suffisamment d’espace, commençons par un nouveau VB. Nous ne voulons pas utiliser la même valeur, car il peut y avoir une opération DMA en cours. Nous communiquons cela à Direct3D et au pilote en verrouillant le même VB avec l' \_ indicateur D3DLOCK Discard. C’est ce que signifie « vous pouvez me faire un nouveau pointeur, car j’en ai terminé avec l’ancien et ne m’intéresse plus à l’ancien contenu ».
12. I = 0.
13. Goto 4 (ou 6).

</dd> <dt>

<span id="Why_do_I_have_to_specify_more_information_in_the_D3DVERTEXELEMENT9_structure__"></span><span id="why_do_i_have_to_specify_more_information_in_the_d3dvertexelement9_structure__"></span><span id="WHY_DO_I_HAVE_TO_SPECIFY_MORE_INFORMATION_IN_THE_D3DVERTEXELEMENT9_STRUCTURE__"></span>**Pourquoi dois-je spécifier des informations supplémentaires dans la structure D3DVERTEXELEMENT9 ?** 
</dt> <dd>

À partir de Direct3D 9, la déclaration de flux de vertex n’est plus simplement un tableau de DWORD, il s’agit maintenant d’un tableau de structures D3DVERTEXELEMENT9. Le runtime utilise les informations sémantiques et d’utilisation supplémentaires pour lier le contenu des flux de vertex aux registres d’entrée/variables. Pour Direct3D 9, les déclarations de vertex sont découplées à partir des nuanceurs vertex, ce qui facilite l’utilisation de nuanceurs avec des géométries de différents formats, car le runtime lie uniquement les données dont le nuanceur a besoin.

Les nouvelles déclarations de vertex peuvent être utilisées avec le pipeline de fonction fixe ou avec les nuanceurs. Pour le pipeline de fonction fixe, il n’est pas nécessaire d’appeler SetVertexShader. Si toutefois vous souhaitez basculer vers le pipeline de fonctions fixe et que vous avez précédemment utilisé un nuanceur de sommets, appelez SetVertexShader (NULL). Une fois cette opération effectuée, vous devrez toujours appeler SetFVF pour déclarer le code de la Commission.

Quand vous utilisez des nuanceurs vertex, appelez SetVertexShader avec l’objet vertex shader. En outre, appelez SetFVF pour configurer une déclaration de vertex. Cela utilise les informations implicites dans le prix de la Commission. SetVertexDeclaration peut être appelé à la place de SetFVF, car il prend en charge les déclarations de vertex qui ne peuvent pas être exprimées avec une Commission de la Commission.

</dd> </dl>

### <a name="d3dx-utility-library"></a>Bibliothèque de l’utilitaire D3DX

<dl> <dt>

<span id="What_file_formats_are_supported_by_the_D3DX_image_file_loader_functions__"></span><span id="what_file_formats_are_supported_by_the_d3dx_image_file_loader_functions__"></span><span id="WHAT_FILE_FORMATS_ARE_SUPPORTED_BY_THE_D3DX_IMAGE_FILE_LOADER_FUNCTIONS__"></span>**Quels sont les formats de fichiers pris en charge par les fonctions D3DX image file Loader ?** 
</dt> <dd>

Les fonctions D3DX image file Loader prennent en charge les fichiers BMP, TGA, JPG, DIB, PPM et DDS.

</dd> <dt>

<span id="The_text_rendering_functions_in_D3DX_don_t_seem_to_work__what_am_I_doing_wrong__"></span><span id="the_text_rendering_functions_in_d3dx_don_t_seem_to_work__what_am_i_doing_wrong__"></span><span id="THE_TEXT_RENDERING_FUNCTIONS_IN_D3DX_DON_T_SEEM_TO_WORK__WHAT_AM_I_DOING_WRONG__"></span>**Les fonctions de rendu de texte dans D3DX ne semblent pas fonctionner, que dois-je faire ?** 
</dt> <dd>

Une erreur courante lors de l’utilisation des fonctions ID3DXFont ::D rawText consiste à spécifier un composant alpha zéro pour le paramètre Color ; ce qui donne un texte complètement transparent (c’est-à-dire invisible). Pour le texte entièrement opaque, assurez-vous que le composant alpha du paramètre Color est entièrement saturé (255).

</dd> <dt>

<span id="How_can_I_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="how_can_i_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="HOW_CAN_I_SAVE_THE_CONTENTS_OF_A_SURFACE_OR_TEXTURE_TO_A_FILE__"></span>**Comment puis-je enregistrer le contenu d’une surface ou d’une texture dans un fichier ?** 
</dt> <dd>

Le kit de développement logiciel (SDK) DirectX 8,1 a ajouté deux fonctions à la bibliothèque D3DX spécifiquement à cet effet : D3DXSaveSurfaceToFile () et D3DXSaveTextureToFile (). Ces fonctions prennent en charge l’enregistrement d’une image dans un fichier au format BMP ou DDS. Dans les versions précédentes, vous devrez verrouiller la surface et lire les données de l’image, puis les écrire dans un fichier bitmap. Pour plus d’informations sur l’écriture d’une fonction pour stocker des bitmaps, consultez [stockage d’une image](/windows/desktop/gdi/storing-an-image).

GDI+ peut également être utilisé pour enregistrer l’image dans un grand nombre de formats, même si cela nécessite la distribution de fichiers de prise en charge supplémentaires avec votre application.

</dd> <dt>

<span id="How_can_I_make_use_of_the_High_Level_Shader_Language__HLSL__in_my_game__"></span><span id="how_can_i_make_use_of_the_high_level_shader_language__hlsl__in_my_game__"></span><span id="HOW_CAN_I_MAKE_USE_OF_THE_HIGH_LEVEL_SHADER_LANGUAGE__HLSL__IN_MY_GAME__"></span>**Comment faire pour utiliser le HLSL (High Level Shader Language) dans mon jeu ?** 
</dt> <dd>

Il existe trois façons d’incorporer le langage HLSL (High Level Shader Language) Microsoft dans votre moteur de jeu :

-   Compilez votre source de nuanceur dans un assembly d’ombrage de pixel ou de vertex (à l’aide de l’utilitaire de ligne de commande fxc.exe) et utilisez D3DXAssembleShader () au moment de l’exécution. Ainsi, même un jeu DirectX 8 peut même tirer parti de la puissance du langage HLSL.
-   Utilisez D3DXCompileShader () pour compiler votre source de nuanceur dans un flux de jetons et un formulaire de table constante. Au moment de l’exécution, chargez le flux de jetons et la table constante, puis appelez CreateVertexShader () ou CreatePixelShader () sur l’appareil pour créer vos nuanceurs.
-   Le moyen le plus simple d’être opérationnel consiste à tirer parti du système D3DX Effects en appelant D3DXCreateEffectFromFile () ou D3DXCreateEffectFromResource () avec votre fichier Effect.

</dd> <dt>

<span id="What_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="what_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_NEW_SHADER_COMPILER_FLAG__"></span>**Quel est l’objectif du nouvel indicateur de compilateur de nuanceur ?** 
</dt> <dd>

À partir du kit de développement logiciel (SDK) DirectX du 2006 décembre, le nouveau compilateur HLSL développé pour Direct3D 10 a été activé pour les cibles Direct3D 9. Le nouveau compilateur n’a pas de prise en charge pour \_ \_ les cibles PS 1 x et est maintenant le compilateur par défaut pour tous les nuanceurs HLSL Direct3D. Un indicateur de compatibilité descendante peut être utilisé pour forcer \_ \_ les cibles PS 1 x à compiler en tant que \_ cibles PS 2 \_ 0.

Les applications qui souhaitent utiliser le compilateur hérité peuvent continuer à le faire en fournissant un indicateur au moment de l’exécution (voir [**indicateurs du compilateur**](/windows/desktop/direct3d9/d3dxshader-flags)) ou en fournissant un commutateur lors de l’utilisation de fxc.

</dd> <dt>

<span id="What_is_the_correct_way_to_get_shaders_from_an_Effect__"></span><span id="what_is_the_correct_way_to_get_shaders_from_an_effect__"></span><span id="WHAT_IS_THE_CORRECT_WAY_TO_GET_SHADERS_FROM_AN_EFFECT__"></span>**Quelle est la méthode correcte pour récupérer les nuanceurs d’un effet ?** 
</dt> <dd>

Utilisez D3DXCreateEffect pour créer un ID3DXEffect, puis utilisez GetPassDesc pour récupérer un D3DXPASS \_ desc. Cette structure contient des pointeurs vers des nuanceurs vertex et de pixels.

N’utilisez pas ID3DXEffectCompiler :: GetPassDesc. Les handles de nuanceur de vertex et de pixels retournés par cette méthode sont NULL.

</dd> <dt>

<span id="What_is_the_HLSL_noise___intrinsic_for__"></span><span id="what_is_the_hlsl_noise___intrinsic_for__"></span><span id="WHAT_IS_THE_HLSL_NOISE___INTRINSIC_FOR__"></span>**Qu’est-ce que l’intrinsèque bruit HLSL () ?** 
</dt> <dd>

La fonction de bruit intrinsèque génère un bruit perl tel que défini par Ken perl. Actuellement, la fonction HLSL ne peut être utilisée que pour remplir des textures dans des nuanceurs de texture, car les h/w actuels ne prennent pas en charge la méthode en mode natif. Les nuanceurs de texture sont utilisés avec les \* fonctions de texture D3DXFill () qui sont des fonctions d’assistance utiles pour générer des textures définies de façon procédurale pendant le temps de chargement.

</dd> <dt>

<span id="How_do_I_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="how_do_i_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="HOW_DO_I_DETECT_WHETHER_TO_USE_PIXEL_SHADER_MODEL_2.0_OR_2.A__"></span>**Comment faire détecter s’il faut utiliser le nuanceur de pixels 2,0 ou 2. a ?** 
</dt> <dd>

Vous pouvez utiliser les fonctions D3DXGetPixelShaderProfile () et D3DXGetPixelShaderProfile () qui retournent une chaîne déterminant le profil HLSL le mieux adapté à l’exécution de l’appareil.

</dd> <dt>

<span id="How_do_I_access_the_Parameters_in_my_Precompiled_Effects_Shaders__"></span><span id="how_do_i_access_the_parameters_in_my_precompiled_effects_shaders__"></span><span id="HOW_DO_I_ACCESS_THE_PARAMETERS_IN_MY_PRECOMPILED_EFFECTS_SHADERS__"></span>**Comment faire accéder aux paramètres dans mes nuanceurs d’effets précompilés ?** 
</dt> <dd>

Via l’interface ID3DXConstantTable qui est utilisée pour accéder à la table constante. Ce tableau contient les variables utilisées par les nuanceurs et les effets de langages de haut niveau.

</dd> <dt>

<span id="Is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="IS_THERE_A_WAY_TO_ADD_USER_DATA_TO_AN_EFFECT_OR_OTHER_RESOURCE__"></span>**Existe-t-il un moyen d’ajouter des données utilisateur à un effet ou à une autre ressource ?** 
</dt> <dd>

Oui, pour définir les données privées que vous appelez SetPrivateData (pReal est l’objet de texture D3D, pSpoof est l’objet de texture encapsulé).

``` syntax
hr = pReal->SetPrivateData(IID_Spoof, &pSpoof, 
            sizeof(IDirect3DResource9*), 0)));
```

Pour rechercher le pointeur encapsulé :

``` syntax
    IDirect3DResource9* pSpoof;
    DWORD dwSize = sizeof(pSpoof);
    hr = pReal->GetPrivateData(IID_Spoof, (void*) &pSpoof, &dwSize);
```

</dd> <dt>

<span id="Why_does_rendering_of_an_ID3DXMesh_object_slow_down_significantly_after_I_define_subsets__"></span><span id="why_does_rendering_of_an_id3dxmesh_object_slow_down_significantly_after_i_define_subsets__"></span><span id="WHY_DOES_RENDERING_OF_AN_ID3DXMESH_OBJECT_SLOW_DOWN_SIGNIFICANTLY_AFTER_I_DEFINE_SUBSETS__"></span>**Pourquoi le rendu d’un objet ID3DXMesh ralentit considérablement après la définition de sous-ensembles ?** 
</dt> <dd>

Vous n’avez probablement pas optimisé la maille après avoir défini les attributs de visage. Si vous spécifiez des attributs, puis appelez ID3DXMesh ::D rawSubset (), cette méthode doit effectuer une recherche dans le maillage pour toutes les faces contenant les attributs demandés. En outre, les visages rendus sont probablement dans un modèle d’accès aléatoire, ce qui n’utilise pas le cache de vertex. Après avoir défini les attributs de visage pour vos sous-ensembles, appelez les méthodes ID3DXMesh :: Optimize ou ID3DXMesh :: OptimizeInPlace et en spécifiant une méthode d’optimisation de D3DXMESHOPT \_ ATTRSORT ou renforcée. Notez que, pour des performances optimales, vous devez optimiser avec l' \_ indicateur D3DXMESHOPT VERTEXCACHE, qui réorganise également les vertex pour une utilisation optimale du cache de vertex. Le tableau d’adjacence généré pour un maillage D3DX comporte trois entrées par face, mais certaines faces peuvent ne pas avoir de faces adjacentes sur les trois bords. Comment ce code est-il encodé ? Les entrées pour lesquelles il n’y a pas de faces adjacentes sont encodées en tant que 0xFFFFFFFF.

</dd> <dt>

<span id="I_ve_heard_a_lot_about_Pre-computed_Radiance_Transfer__PRT___where_can_I_learn_more__"></span><span id="i_ve_heard_a_lot_about_pre-computed_radiance_transfer__prt___where_can_i_learn_more__"></span><span id="I_VE_HEARD_A_LOT_ABOUT_PRE-COMPUTED_RADIANCE_TRANSFER__PRT___WHERE_CAN_I_LEARN_MORE__"></span>**J’ai entendu beaucoup de choses sur le transfert luminance (PRT) précalculé, où puis-je en savoir plus ?** 
</dt> <dd>

PRT est une nouvelle fonctionnalité de D3DX ajoutée dans la mise à jour du kit de développement logiciel (SDK) 2003. Il permet de rendre les scénarios d’éclairage complexes tels que Global-llumination, les instantanés logiciels et les nuages de points de la sous-surface en temps réel. Le kit de développement logiciel (SDK) contient de la documentation et des exemples d’intégration de la technologie dans votre jeu. Les exemples d’exemples PRT et Sample Demo montrent comment utiliser le simulateur pour les scénarios d’éclairage par vertex et par pixel, respectivement. Vous trouverez plus d’informations sur ce sujet et d’autres rubriques sur la page Web de Peter dénominations Sloan.

</dd> <dt>

<span id="How_can_I_render_to_a_texture_and_make_use_of_Anti_Aliasing__"></span><span id="how_can_i_render_to_a_texture_and_make_use_of_anti_aliasing__"></span><span id="HOW_CAN_I_RENDER_TO_A_TEXTURE_AND_MAKE_USE_OF_ANTI_ALIASING__"></span>**Comment puis-je effectuer un rendu sur une texture et utiliser l’anticrénelage ?** 
</dt> <dd>

Créez une cible de rendu à échantillonnage à l’aide de Direct3DDevice9 :: CreateRenderTarget. Après avoir rendu la scène à cette cible de rendu, StretchRect à une texture de cible de rendu. Si vous modifiez les textre hors écran (par exemple, en les flouant ou en les souquient), recopiez-les dans la mémoire tampon d’arrière-plan avant d’avoir présent ().

</dd> </dl>

## <a name="directsound-questions"></a>Questions sur DirectSound

<dl> <dt>

<span id="Why_do_I_get_a_burst_of_static_when_my_application_starts_up__I_notice_this_problem_with_other_applications_too._"></span><span id="why_do_i_get_a_burst_of_static_when_my_application_starts_up__i_notice_this_problem_with_other_applications_too._"></span><span id="WHY_DO_I_GET_A_BURST_OF_STATIC_WHEN_MY_APPLICATION_STARTS_UP__I_NOTICE_THIS_PROBLEM_WITH_OTHER_APPLICATIONS_TOO._"></span>**Pourquoi est-ce que je reçois une rafale de statiques au démarrage de mon application ? Je remarque également ce problème avec d’autres applications.** 
</dt> <dd>

Vous avez probablement installé le runtime DirectX de débogage. La version de débogage du runtime remplit les mémoires tampons statiques afin d’aider les développeurs à détecter les bogues avec des mémoires tampons non initialisées. Vous ne pouvez pas garantir le contenu d’une mémoire tampon DirectSound après sa création ; en particulier, vous ne pouvez pas supposer qu’une mémoire tampon a été mise à zéro.

</dd> <dt>

<span id="Why_I_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="why_i_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="WHY_I_AM_EXPERIENCING_A_DELAY_IN_BETWEEN_CHANGING_AN_EFFECTS_PARAMETERS_AND_HEARING_THE_RESULTS__"></span>**Pourquoi est-ce que je rencontre un décalage entre la modification d’un paramètre d’effet et l’audition des résultats ?** 
</dt> <dd>

Les modifications apportées aux paramètres d’effet n’ont pas toujours lieu immédiatement sur DirectX 8. Pour des performances optimales, DirectSound traite 100 millisecondes de données audio dans une mémoire tampon, en commençant au curseur de lecture avant la lecture de la mémoire tampon. Ce prétraitement se produit après tous les appels suivants :

``` syntax
IDirectSoundBuffer8::SetCurrentPosition
IDirectSoundBuffer8::SetFX
IDirectSoundBuffer8::Stop
IDirectSoundBuffer8::Unlock
```

Depuis DirectX 9, un nouvel algorithme de traitement FX qui traite les effets juste-à-temps résout ce problème et a réduit la latence. L’algorithme a été ajouté à l’appel de IDirectSoundBuffer8 ::P (), avec un thread supplémentaire qui traite les effets juste à l’avance du curseur d’écriture. Vous pouvez ainsi définir des paramètres à tout moment pour qu’ils fonctionnent comme prévu. Toutefois, Notez que sur une mémoire tampon de lecture il y a un petit délai (généralement de 100 ms) avant d’entendre la modification du paramètre, car le contenu audio entre les curseurs de lecture et d’écriture (et un peu plus de remplissage) a déjà été traité à ce moment-là.

</dd> <dt>

<span id="How_do_I_detect_if_DSound_is_installed__"></span><span id="how_do_i_detect_if_dsound_is_installed__"></span><span id="HOW_DO_I_DETECT_IF_DSOUND_IS_INSTALLED__"></span>**Comment faire détecter si DSound est installé ?** 
</dt> <dd>

Si vous n’avez pas besoin d’utiliser DirectSoundEnumerate () pour répertorier les appareils DSound disponibles, ne liez pas votre application à dsound. lib et utilisez-la à la place via les sociétés CoCreateInstance (CLSID \_ DirectSound...), puis initialisez l’objet dsound à l’aide de Initialize (null). Si vous devez utiliser DirectSoundEnumerate (), vous pouvez charger dynamiquement dsound.dll à l’aide de LoadLibrary (« dsound.dll »); et accèdent à ses méthodes à l’aide de GetProcAddress (« DirectSoundEnumerateA/W ») et de GetProcAddress (« DirectSoundCreateA/W »), et ainsi de suite.

</dd> <dt>

<span id="How_do_I_create_multichannel_audio_with_WAVEFORMATEXTENSIBLE__"></span><span id="how_do_i_create_multichannel_audio_with_waveformatextensible__"></span><span id="HOW_DO_I_CREATE_MULTICHANNEL_AUDIO_WITH_WAVEFORMATEXTENSIBLE__"></span>**Comment faire créer un audio multicanal avec WAVEFORMATEXTENSIBLE ?** 
</dt> <dd>

Si vous ne trouvez pas de réponse à votre question dans les fichiers d’aide DirectSound, vous trouverez un bon article contenant des informations supplémentaires sur les données audio et les fichiers WAVE à plusieurs canaux.

</dd> <dt>

<span id="How_can_I_use_the_DirectSound_Voice_Manager_with_property_sets_like_EAX__"></span><span id="how_can_i_use_the_directsound_voice_manager_with_property_sets_like_eax__"></span><span id="HOW_CAN_I_USE_THE_DIRECTSOUND_VOICE_MANAGER_WITH_PROPERTY_SETS_LIKE_EAX__"></span>**Comment puis-je utiliser le gestionnaire de voix DirectSound avec des jeux de propriétés comme EAX ?** 
</dt> <dd>

Dans DirectSound 9,0, lorsque vous dupliquez une mémoire tampon, il est désormais possible d’obtenir l’interface IDirectSoundBuffer8 sur le tampon dupliqué, ce qui vous donne accès à la méthode AcquireResources. Cela vous permettra d’associer une mémoire tampon à l' \_ indicateur DSBCAPS LOCDEFER à une ressource matérielle. Vous pouvez ensuite définir vos paramètres EAX sur cette mémoire tampon avant d’avoir à appeler Play ().

</dd> <dt>

<span id="I_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._How_can_I_get_more_accurate_information__"></span><span id="i_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._how_can_i_get_more_accurate_information__"></span><span id="I_AM_HAVING_PROBLEMS_WITH_UNRELIABLE_BEHAVIOR_WHEN_USING_CURSOR_POSITION_NOTIFICATIONS._HOW_CAN_I_GET_MORE_ACCURATE_INFORMATION__"></span>**Je rencontre des problèmes de comportement non fiable lors de l’utilisation de notifications de position de curseur. Comment puis-je obtenir des informations plus précises ?** 
</dt> <dd>

Il existe des bogues subtils dans différentes versions de DirectSound, la pile audio principale Windows et les pilotes audio qui rendent les notifications de position de curseur non fiables. À moins que vous ne cibliez une configuration matérielle/logicielle connue sur laquelle vous savez que les notifications sont bien connues, évitez les notifications de position de curseur. Pour le suivi de position, GetCurrentPosition () est une technique plus sûre.

</dd> <dt>

<span id="I_am_suffering_from_performance_degradation_when_using_GetCurrentPosition__._What_can_I_do_to_improve_performance__"></span><span id="i_am_suffering_from_performance_degradation_when_using_getcurrentposition__._what_can_i_do_to_improve_performance__"></span><span id="I_AM_SUFFERING_FROM_PERFORMANCE_DEGRADATION_WHEN_USING_GETCURRENTPOSITION__._WHAT_CAN_I_DO_TO_IMPROVE_PERFORMANCE__"></span>**Je suis victime d’une dégradation des performances lors de l’utilisation de GetCurrentPosition (). Que puis-je faire pour améliorer les performances ?** 
</dt> <dd>

Chaque appel GetCurrentPosition () sur chaque mémoire tampon provoque un appel système et les appels système doivent être minimisés, car ils constituent un composant important de l’encombrement du processeur de DSound. Sur NT (Win2K et XP), les curseurs dans les tampons de logiciels (et les tampons matériels sur certains appareils) se déplacent en incréments de 10 ms, de sorte que l’appel de GetCurrentPosition () chaque 10 ms est idéal. L’appeler plus souvent que chaque 5 ms entraîne une dégradation des performances.

</dd> <dt>

<span id="My_DirectSound_application_is_taking_up_too_much_CPU_time_or_is_performing_slowly._Is_there_anything_I_can_do_to_optimize_my_code__"></span><span id="my_directsound_application_is_taking_up_too_much_cpu_time_or_is_performing_slowly._is_there_anything_i_can_do_to_optimize_my_code__"></span><span id="MY_DIRECTSOUND_APPLICATION_IS_TAKING_UP_TOO_MUCH_CPU_TIME_OR_IS_PERFORMING_SLOWLY._IS_THERE_ANYTHING_I_CAN_DO_TO_OPTIMIZE_MY_CODE__"></span>**Mon application DirectSound prend trop de temps processeur ou s’exécute lentement. Y a-t-il quelque chose que je peux faire pour optimiser mon code ?** 
</dt> <dd>

Vous pouvez effectuer plusieurs opérations pour améliorer les performances de votre code audio :

-   N’appelez pas GetCurrentPosition trop souvent. Chaque appel GetCurrentPosition () sur chaque mémoire tampon provoque un appel système et les appels système doivent être minimisés, car ils constituent un composant important de l’encombrement du processeur de DSound. Sur NT (Win2K et XP), les curseurs dans les tampons de logiciels (et les tampons matériels sur certains appareils) se déplacent en incréments de 10 ms, de sorte que l’appel de GetCurrentPosition () chaque 10 ms est idéal. L’appeler plus souvent que chaque 5 ms entraîne une dégradation des performances.
-   Utilisez une fréquence d’images distincte et inférieure pour les données audio. Aujourd’hui, de nombreux jeux Windows peuvent dépasser 100 images par seconde et il n’est pas nécessaire, dans la plupart des cas, de mettre à jour vos paramètres audio 3D à la même fréquence d’images. Le traitement de votre audio chaque seconde ou troisième image graphique, ou tous les 30ms, peut réduire le nombre d’appels audio de manière significative dans votre application sans réduire la qualité audio.
-   Utilisez DS3D \_ différé pour les objets 3D. La plupart des cartes audio répondent immédiatement aux modifications de paramètres et, dans une seule image, la plupart peuvent changer, en particulier si vous modifiez la position ou l’orientation de l’écouteur. Cela amène la carte son/UC à effectuer de nombreux calculs inutiles. par conséquent, une autre optimisation rapide et universelle consiste à différer certaines modifications de paramètres et à les valider à la fin du frame.

    au moins, utilisez SetAllParameters plutôt que des appels Set3DParamX individuels sur des mémoires tampons.

    De même, vous devez utiliser au moins les appels SetAllParamenters sur les mémoires tampons 3D au lieu des appels Set3DParamX individuels. Essayez simplement de réduire les appels système chaque fois que cela est possible.

-   Ne pas effectuer d’appels redondants ; stockez et triez une liste d’appels de lecture. Souvent, dans une image de mise à jour Audio, il y a 2 requêtes pour lire de nouveaux sons. Si les demandes sont traitées au fur et à mesure qu’elles arrivent, le premier nouveau son est démarré, puis remplacé immédiatement le deuxième son demandé. Cela entraîne des calculs redondants, un appel de lecture inutile et un appel d’arrêt inutile. Il est préférable de stocker une liste de demandes de nouveaux sons à lire, de sorte que la liste puisse être triée et que seules les voix qui devraient commencer à jouer soient réellement lues.

    En outre, vous devez stocker des copies locales des paramètres 3D et EAX pour chaque source audio. Si une demande est effectuée pour définir un paramètre sur une valeur particulière, vous pouvez vérifier si la valeur est en fait différente de la dernière valeur définie. Si ce n’est pas le cas, l’appel n’a pas besoin d’être effectué.

    Bien que le pilote de carte son détectera probablement ce scénario et n’effectuera pas à nouveau le calcul (identique), l’appel audio devra atteindre le pilote audio (via une transition en anneau) et cette opération est déjà lente.

</dd> <dt>

<span id="When_I_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._What_s_the_best_way_to_stream_a_buffer__"></span><span id="when_i_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._what_s_the_best_way_to_stream_a_buffer__"></span><span id="WHEN_I_STREAM_A_BUFFER_IT_TENDS_TO_GLITCH_AND_PERFORM_POORLY._WHAT_S_THE_BEST_WAY_TO_STREAM_A_BUFFER__"></span>**Lorsque je diffuse un tampon, il a tendance à se lancer et à fonctionner mal. Quelle est la meilleure façon de diffuser une mémoire tampon ?** 
</dt> <dd>

Lorsque vous diffusez du contenu audio dans une mémoire tampon, il existe deux algorithmes de base : après-écriture-curseur (AWC) et avant-lecture-curseur (BPC). AWC minimise la latence au détriment du problème, tandis que BPC est le contraire. Étant donné qu’il n’y a généralement pas de modifications interactives du son diffusé en continu, ce type de latence est rarement un problème pour les jeux et les applications similaires, c’est pourquoi BPC est l’algorithme le plus approprié. Dans AWC, chaque fois que votre thread de diffusion en continu exécute « haut » les données de vos mémoires tampons de bouclage jusqu’à N MS au-delà de leurs curseurs d’écriture (généralement N = 40, pour permettre l’instabilité de la planification Windows). Dans BPC, vous écrivez toujours autant de données que possible dans les mémoires tampons, en les remplissant jusqu’à leurs curseurs de lecture (ou peut-être 32 octets avant de permettre aux pilotes qui signalent incorrectement leur progression du curseur de lecture).

Utilisez BPC pour mimimize les problèmes et utilisez des mémoires tampons de 100 $ ou plus, même si vos jeux ne se déposent pas sur votre matériel de test, cela entraînera un problème sur certaines machines.

</dd> <dt>

<span id="I_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_Play___call_takes_a_long_time._What_should_I_do__"></span><span id="i_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_play___call_takes_a_long_time._what_should_i_do__"></span><span id="I_AM_PLAYING_THE_SAME_SOUNDS_OVER_AND_OVER_VERY_OFTEN_AND_VERY_QUICKLY_AND_SOMETIMES_THEY_DON_T_PLAY_PROPERLY__OR_THE_PLAY___CALL_TAKES_A_LONG_TIME._WHAT_SHOULD_I_DO__"></span>**Je joue les mêmes sons, très souvent et très rapidement et parfois, ils ne s’exécutent pas correctement, ou l’appel de lecture () prend beaucoup de temps. Que dois-je faire ?** 
</dt> <dd>

La latence de démarrage (différente de la latence de diffusion mentionnée ci-dessus) peut être un problème dans le cas d’un matériel (l’appel de lecture () prend parfois beaucoup de temps sur certaines cartes son). Si vous voulez vraiment réduire cette latence, pour les sons Twitch (captures de pistolet, traces, etc.), une astuce pratique consiste à conserver des mémoires tampons toujours en boucle et à jouer un silence. Lorsque vous avez besoin de lire un son Twitch, de choisir un tampon libre, de voir où se trouve son curseur d’écriture et de placer le son dans la mémoire tampon juste après le curseur d’écriture. Certains Soundcards échouent QuerySupport pour les propriétés différées que je sais qu’elles prennent en charge. Existe-t-il une solution de contournement ? Vous pouvez simplement QuerySupport pour les versions non différées des propriétés et utiliser les paramètres différés quand même. Les pilotes carte son les plus récents peuvent également résoudre ce problème.

</dd> <dt>

<span id="How_do_I_encode_WAV_files_into_WMA__"></span><span id="how_do_i_encode_wav_files_into_wma__"></span><span id="HOW_DO_I_ENCODE_WAV_FILES_INTO_WMA__"></span>**Comment faire encoder les fichiers WAV en WMA ?** 
</dt> <dd>

Reportez-vous à la documentation sur l’encodeur Windows Media à l’adresse suivante : Windows Media Encoder 9 Series.

</dd> <dt>

<span id="How_do_I_decode_MP3_files_with_DirectSound__"></span><span id="how_do_i_decode_mp3_files_with_directsound__"></span><span id="HOW_DO_I_DECODE_MP3_FILES_WITH_DIRECTSOUND__"></span>**Comment faire décoder des fichiers MP3 avec DirectSound ?** 
</dt> <dd>

DirectSound ne prend pas en charge le décodage MP3 en mode natif. Vous pouvez décoder les fichiers à l’avance vous-même (à l’aide d’un codec ACM d’un filtre DirectShow), ou simplement utiliser DirectShow lui-même, ce qui peut vous permettre d’effectuer le décodage. vous pouvez ensuite copier les données audio PCM obtenues dans vos mémoires tampons DirectSound.

</dd> </dl>

## <a name="directx-extensions-for-alias-maya"></a>Extensions DirectX pour Alias Maya

<dl> <dt>

<span id="Why_aren_t_my_NURBS_showing_up__"></span><span id="why_aren_t_my_nurbs_showing_up__"></span><span id="WHY_AREN_T_MY_NURBS_SHOWING_UP__"></span>**Pourquoi mon NURBS ne s’affiche-t-il pas ?** 
</dt> <dd>

Les NURBS ne sont pas pris en charge. Vous pouvez les convertir en maillages de polygones.

</dd> <dt>

<span id="Why_aren_t_my_SUBDs_showing_up_"></span><span id="why_aren_t_my_subds_showing_up_"></span><span id="WHY_AREN_T_MY_SUBDS_SHOWING_UP_"></span>**Pourquoi mes SUBDs ne s’affichent-ils pas ?**
</dt> <dd>

Les SUBDs ne sont pas pris en charge. Vous pouvez les convertir en maillages de polygones.

</dd> <dt>

<span id="Why_does_my_animation_in_the_X_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="why_does_my_animation_in_the_x_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="WHY_DOES_MY_ANIMATION_IN_THE_X_FILE_LOOK_DIFFERENT_THAN_THE_ANIMATION_IN_THE_PREVIEW_WINDOW__"></span>**Pourquoi mon animation dans le fichier X a-t-elle un aspect différent de l’animation dans la fenêtre d’aperçu ?** 
</dt> <dd>

La fenêtre d’aperçu n’est pas animée dans le sens le plus strict de la question. Elle ne lit pas l’animation, mais se synchronise à l’état le plus récent de la scène de Maya. Lorsque l’animation est exportée, les matrices à chaque transformation sont décomposées en composants d’échelle, de rotation (Quaternion) et de translation (souvent appelés SRTs). Les SRTs sont plus souhaitables que les matrices car elles interpolent bien, fournissent une forme plus compacte des données et peuvent être compressées indépendamment. Toutes les matrices ne peuvent pas se scinder en SRTs. S’ils ne peuvent pas se décomposer, le SRTs résultant est inconnu, si bien que de petites erreurs dans l’animation peuvent être détectées. Les deux fonctionnalités de maya qui causent le plus souvent des problèmes au cours de la décomposition sont les cisailles et les rotations ou les échelles hors Centre. Si vous rencontrez ce problème, car vous utilisez des rotations ou des échelles hors Centre, pensez à ajouter des transformations supplémentaires qui augmentent votre niveau de hiérarchie.

Lorsque l’animation D3DX prend en charge SRTs, elle ressemble à ceci :

``` syntax
[S]x[R]x[T]
```

Les matrices de Maya sont beaucoup plus compliquées et nécessitent une quantité importante de processus supplémentaires, qui ressemble à ceci :

``` syntax
[SpInv]x[S]x[Sh]x[Sp]x[St]x[RpInv]x[Ro]x[R]x[Rp]x[Rt]x[T]
```

</dd> <dt>

<span id="I_skinned_my_mesh_with_RigidSkin_but_the_mesh__or_portion__isn_t_moving._Why__"></span><span id="i_skinned_my_mesh_with_rigidskin_but_the_mesh__or_portion__isn_t_moving._why__"></span><span id="I_SKINNED_MY_MESH_WITH_RIGIDSKIN_BUT_THE_MESH__OR_PORTION__ISN_T_MOVING._WHY__"></span>**J’ai dépouillé mon treillis avec RigidSkin mais la maille (ou la partie) ne bouge pas. Pourquoi?** 
</dt> <dd>

L’apparence rigide de Maya n’est pas prise en charge pour l’instant. Utilisez l’apparence lisse.

</dd> <dt>

<span id="Where_has_all_of_my_IK_gone_in_the_X-file__"></span><span id="where_has_all_of_my_ik_gone_in_the_x-file__"></span><span id="WHERE_HAS_ALL_OF_MY_IK_GONE_IN_THE_X-FILE__"></span>**Où tout mon IK a-t-il disparu dans le fichier X ?** 
</dt> <dd>

Les fichiers X ne prennent pas en charge IK. Au lieu de cela, les solutions IK sont intégrées aux images stockées dans le fichier X.

</dd> <dt>

<span id="Why_do_none_of_my_materials_colors_show_up_except_DirectXShaders__"></span><span id="why_do_none_of_my_materials_colors_show_up_except_directxshaders__"></span><span id="WHY_DO_NONE_OF_MY_MATERIALS_COLORS_SHOW_UP_EXCEPT_DIRECTXSHADERS__"></span>**Pourquoi les couleurs de mes matériaux ne sont-elles pas affichées, à l’exception de DirectXShaders ?** 
</dt> <dd>

Les extensions DirectX pour Maya ne prennent actuellement en charge que les documents DirectXShader pour l’aperçu et l’exportation. Dans une version ultérieure, d’autres documents peuvent être pris en charge.

</dd> </dl>

## <a name="xinput-questions"></a>Questions XInput

<dl> <dt>

<span id="Can_I_use_DirectInput_to_read_the_triggers__"></span><span id="can_i_use_directinput_to_read_the_triggers__"></span><span id="CAN_I_USE_DIRECTINPUT_TO_READ_THE_TRIGGERS__"></span>**Puis-je utiliser DirectInput pour lire les déclencheurs ?** 
</dt> <dd>

Oui, mais ils agissent comme le même axe. Vous ne pouvez donc pas lire les déclencheurs indépendamment avec DirectInput. À l’aide de XInput, les déclencheurs retournent des valeurs distinctes.

Pour plus d’informations sur la raison pour laquelle DirectInput interprète les déclencheurs comme un seul axe, consultez [utilisation du contrôleur Xbox 360 avec DirectInput](/windows/desktop/xinput/xinput-and-directinput).

</dd> <dt>

<span id="How_many_controllers_does_XInput_support__"></span><span id="how_many_controllers_does_xinput_support__"></span><span id="HOW_MANY_CONTROLLERS_DOES_XINPUT_SUPPORT__"></span>**Quel est le nombre de contrôleurs pris en charge par XInput ?** 
</dt> <dd>

XInput prend en charge 4 contrôleurs branchés à la fois.

</dd> <dt>

<span id="Does_XInput_support_non-common_controllers__"></span><span id="does_xinput_support_non-common_controllers__"></span><span id="DOES_XINPUT_SUPPORT_NON-COMMON_CONTROLLERS__"></span>**XInput prend-il en charge les contrôleurs non communs ?** 
</dt> <dd>

Non, ce n’est pas le cas.

</dd> <dt>

<span id="Are_common_controllers_available_through_DirectInput__"></span><span id="are_common_controllers_available_through_directinput__"></span><span id="ARE_COMMON_CONTROLLERS_AVAILABLE_THROUGH_DIRECTINPUT__"></span>**Des contrôleurs communs sont-ils disponibles via DirectInput ?** 
</dt> <dd>

Oui, vous pouvez accéder aux contrôleurs communs via DirectInput.

</dd> <dt>

<span id="How_do_I_get_force_feedback_on_the_common_controllers__"></span><span id="how_do_i_get_force_feedback_on_the_common_controllers__"></span><span id="HOW_DO_I_GET_FORCE_FEEDBACK_ON_THE_COMMON_CONTROLLERS__"></span>**Comment faire obtenir des retours de force sur les contrôleurs courants ?** 
</dt> <dd>

Utilisez la fonction [**XInputSetState**](/windows/desktop/api/xinput/nf-xinput-xinputsetstate) .

</dd> <dt>

<span id="Why_does_my_default_audio_device_change__"></span><span id="why_does_my_default_audio_device_change__"></span><span id="WHY_DOES_MY_DEFAULT_AUDIO_DEVICE_CHANGE__"></span>**Pourquoi mon périphérique audio par défaut change-t-il ?** 
</dt> <dd>

Lors de la connexion du casque, le casque du contrôleur agit comme un périphérique audio USB standard, donc lorsqu’il est connecté, Windows change automatiquement pour utiliser ce périphérique audio USB comme périphérique par défaut. Dans la mesure où l’utilisateur ne veut pas que tous les éléments audio passent par le casque, il devra le rétablir manuellement à sa valeur d’origine.

</dd> <dt>

<span id="How_do_I_control_the_lights_on_the_controller__"></span><span id="how_do_i_control_the_lights_on_the_controller__"></span><span id="HOW_DO_I_CONTROL_THE_LIGHTS_ON_THE_CONTROLLER__"></span>**Comment faire contrôler les lumières du contrôleur ?** 
</dt> <dd>

Les lumières sur le contrôleur sont prédéterminées par le système d’exploitation et ne peuvent pas être modifiées.

</dd> <dt>

<span id="How_do_I_access_the_Xbox_360_button_in_my_applications__"></span><span id="how_do_i_access_the_xbox_360_button_in_my_applications__"></span><span id="HOW_DO_I_ACCESS_THE_XBOX_360_BUTTON_IN_MY_APPLICATIONS__"></span>**Comment faire accéder au bouton Xbox 360 dans mes applications ?** 
</dt> <dd>

Ce bouton est réservé à une utilisation ultérieure.

</dd> <dt>

<span id="Where_do_I_get_drivers__"></span><span id="where_do_i_get_drivers__"></span><span id="WHERE_DO_I_GET_DRIVERS__"></span>**Où puis-je me procurer des pilotes ?** 
</dt> <dd>

Les pilotes seront disponibles via Windows Update.

</dd> <dt>

<span id="How_is_controller_ID_determined__"></span><span id="how_is_controller_id_determined__"></span><span id="HOW_IS_CONTROLLER_ID_DETERMINED__"></span>**Comment l’ID de contrôleur est-il déterminé ?** 
</dt> <dd>

Au démarrage de XInput, l’ID est déterminé de façon non déterministe par le moteur XInput et les contrôleurs qui sont branchés. Si les contrôleurs sont branchés pendant qu’une application XInput est en cours d’exécution, le système affecte au nouveau contrôleur le plus petit nombre disponible. Si un contrôleur est déconnecté, son numéro sera à nouveau disponible.

</dd> <dt>

<span id="How_do_I_get_the_audio_devices_for_the_controller__"></span><span id="how_do_i_get_the_audio_devices_for_the_controller__"></span><span id="HOW_DO_I_GET_THE_AUDIO_DEVICES_FOR_THE_CONTROLLER__"></span>**Comment faire obtenir les périphériques audio pour le contrôleur ?** 
</dt> <dd>

Utilisez la fonction [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/xinput/nf-xinput-xinputgetdsoundaudiodeviceguids) . Pour plus d’informations, consultez l’exemple AudioController.

</dd> <dt>

<span id="What_should_I_do_when_a_controller_is_unplugged__"></span><span id="what_should_i_do_when_a_controller_is_unplugged__"></span><span id="WHAT_SHOULD_I_DO_WHEN_A_CONTROLLER_IS_UNPLUGGED__"></span>**Que dois-je faire lorsqu’un contrôleur est débranché ?** 
</dt> <dd>

Si le contrôleur était utilisé par un joueur, vous devez suspendre le jeu jusqu’à ce que le contrôleur soit reconnecté et que le joueur appuie sur un bouton pour signaler qu’il est prêt à être mis en pause.

</dd> </dl>

 

 