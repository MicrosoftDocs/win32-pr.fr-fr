---
description: Fiabilité et sécurité
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Fiabilité et sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0f0e4a244de2c1463cdadb76162c18b041812b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530890"
---
# <a name="reliability-and-security"></a>Fiabilité et sécurité

Étant donné que les codecs du composant Windows Imaging Component (WIC) sont appelés à partir de l’interpréteur de commandes Windows et de la Galerie de photos, les auteurs de codec doivent faire tout leur possible pour garantir un haut niveau de fiabilité et de sécurité dans leurs codecs WIC.

L’écriture de code fiable dépend en grande partie des bonnes pratiques de codage, des revues de code efficaces et des tests d’unités rigoureux et des tests de scénario. En outre, les instructions suivantes permettent de s’assurer que le codec est conforme aux stratégies Windows Vista en matière de fiabilité.

-   Activez l’annulation d’e/s.

    Les auteurs de codec doivent permettre à l’utilisateur final d’annuler toute opération de longue durée. Les codecs WIC le prennent en charge en implémentant IWICBitmapProgressNotification. Cela permet à une application appelante de spécifier une fonction de rappel que le codec doit appeler à des intervalles spécifiés pour notifier l’appelant de la progression de l’opération en cours. Lorsqu’une application retourne l’erreur \_ annulée à partir de la fonction de rappel, le codec doit annuler l’opération en cours et répartir le HRESULT vers l’appelant. Ceci est particulièrement important pour les codecs BRUTs, car il peut s’avérer nécessaire de prendre plusieurs secondes pour décoder une image brute de taille réelle et les applications ont besoin d’un moyen d’abandonner ce traitement.

-   Assurez-vous que le code s’exécute dans la plus petite portée requise pour exécuter sa fonction.

    Les auteurs de codec doivent s’assurer que le codec ne consomme pas plus de ressources que nécessaire, ou avoir une étendue supérieure à celle requise. La portée d’un codec dans WIC est un fichier image unique. le codec est créé lors du chargement d’un fichier image et le codec est libéré lorsque l’image est fermée. Étant donné que WIC est une plateforme extensible basée sur des composants, les codecs WIC comportent des chargements et des déchargements qui se chevauchent, et démarrent et s’arrêtent, le tout dans le même processus. Si l’infrastructure sous-jacente d’un codec nécessite des opérations de démarrage et d’arrêt dans une étendue supérieure à une seule image, la fiabilité sera affectée. Les codecs compatibles WIC seront utilisés par l’Explorateur Windows, ainsi que par d’autres applications. Par conséquent, si un codec reste chargé pendant la durée de vie du processus, la mémoire n’est pas libérée efficacement et une défaillance du codec peut bloquer l’Explorateur Windows et éventuellement nécessiter le redémarrage de l’ordinateur. (Tenez compte du fait que le codec est appelé chaque fois qu’une image est miniature pour la première fois dans l’Explorateur Windows : il est essentiel qu’il s’agit d’une opération légère.)

-   Utilisez les outils d’analyse du code statiques et dynamiques.

    -   Outils d’analyse statique :

        PREfix : pour détecter les erreurs au moment de la compilation.

        PREfast : pour l’analyse du code pour les bogues.

    -   Outils d’analyse dynamique :

        AppVerifier-qui permet de rendre les applications plus résilientes en simulant des problèmes logiciels courants.

-   Vérifiez toutes les entrées dans les révisions du code.

    Tous les paramètres pour les méthodes exportées et toutes les données de fichier doivent être vérifiés avec soin pour la validité et rejetés de manière fiable en cas de défaillance, afin de se protéger contre les dépassements de mémoire tampon et les sous-exécutions, les dépassements arithmétiques et les dépassements de capacité et les types inattendus

-   Utilisez des techniques de fuzzing de fichiers pour détecter les blocages potentiels et les blocages.

    Le fuzzing de fichier est le processus de test du codec avec des entrées aléatoires.

    Il existe deux formes de fuzzing de fichiers : le fuzzing (aléatoire) et le fuzzing dirigé. Le fuzzing non dirigé effectue un basculement binaire aléatoire pour voir si une entrée aléatoire peut bloquer le codec. Le fuzzing dirigé permute l’entrée en fonction d’une connaissance du format de fichier. Par exemple, s’il existe un contrôle de redondance cyclique (CRC) à l’offset d’octet 32, la modification des octets sans mettre à jour le CRC risque de ne pas exercer la plupart des chemins. Dans cet exemple, un fuzzer dirigé doit corriger le CRC lorsque des octets sont modifiés.

    Le jeu d’images d’entrée pour le fuzzing de fichier doit être créé afin que chaque combinaison de paramètres prise en charge par le décodeur soit testée. Par exemple, si le décodeur prend en charge les fichiers Little-et Big-endian et trois paramètres de compression, le jeu d’images d’entrée doit être composé de fichiers Little endian de chaque paramètre de compression et de fichiers de poids fort (Big-endian) pour chaque paramètre de compression. Cette approche produira un ensemble d’images d’entrée très robustes à tester. Même si aucune caméra ne produit chacune des combinaisons, mais que le décodeur prend en charge ces combinaisons théoriques, les auteurs de codec doivent fuzzer ces entrées.

    La sécurité peut être beaucoup améliorée en effectuant régulièrement un test Fuzz des fichiers image pendant le développement de codec. Les codecs doivent toujours pouvoir détecter l’endommagement du fichier image et échouer correctement dans le cas d’une demande incorrecte ou de données incorrectes.

-   Insistez sur le code.

    Stress-testez le codec en l’exécutant en continu dans plusieurs processus simultanés, en effectuant toutes les opérations prises en charge dans toutes les séquences possibles, sur des images de tailles différentes (y compris des images très volumineuses) à partir de chaque caméra prise en charge.

-   Sécurité des threads.

    À compter de Windows 7, WIC exige que les CODECs BRUTs soient de type cloisonnement COM « both ». Cela signifie que vous devez effectuer le verrouillage approprié pour gérer les appelants inter-cloisonnement et les appelants dans les scénarios multithread. Les objets d’un cloisonnement multithread (MTA) peuvent être appelés simultanément par un nombre quelconque de threads dans le MTA, ce qui permet de meilleures performances sur les systèmes à plusieurs cœurs et certains scénarios de serveur. En outre, les CODECs WIC qui résident dans un MTA peuvent appeler d’autres objets qui résident dans le MTA sans le coût de marshaling associé à l’appel entre les threads qui résident dans différents Apartments STA. Dans Windows 7, tous les CODECs WIC intégrés ont été mis à jour pour prendre en charge les MTA, y compris JPEG, TIFF, PNG, GIF, ICO et BMP. les CODECs tiers qui ne prennent pas en charge les MTA entraînent des coûts de performances significatifs dans les applications multithread en raison du marshaling. L’activation de la prise en charge de MTA nécessite une synchronisation appropriée à implémenter dans le CODEC tiers. L’implémentation exacte de ces techniques de synchronisation dépasse le cadre de ce document. Vous trouverez ci-dessous une référence générale pour la synchronisation des objets COM.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



