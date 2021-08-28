---
description: 'En savoir plus sur : JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: dee8dc7850cf69957c360253b942117739fe405b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987552"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_errcat"></a>JET_ERRCAT

Le **JET_ERRCAT** groupe de constantes décrit les classifications ou les catégories d’erreurs de niveau supérieur. Ce groupe de constantes permet aux applications de définir le traitement par défaut pour une classification des erreurs, au lieu de gérer chaque cas d’erreur individuellement. Elle garantit également que l’application n’a pas à gérer les nouvelles conditions d’erreur incluses dans les classifications existantes.

remarque : cette documentation est basée sur une version préliminaire du moteur de Stockage Extensible. Ces informations sont susceptibles d’être modifiées.

Les constantes de **JET_ERRCAT** sont organisées dans une hiérarchie spécifique de conditions et de sous-conditions, comme suit :

| Erreur---| opération de---(Al) | |---irrécupérable | |---e/s | |---ressource | |---de la mémoire | |---quota | |---disque | |---des données | |---de l’altération | |---incohérent | |---de la fragmentation | |---l’API | utilisation de---

Le tableau suivant répertorie les constantes d' **JET_ERRCAT** et fournit une description et des informations de récupération, le cas échéant.


| <p>Constante/valeur</p> | <p>Description</p> | <p>Récupération</p> | 
|-----------------------|--------------------|-----------------|
| <p>JET_errcatUnknown 0</p> | <p>Catégorie d’erreur non valide.</p> | <p>N/A.</p> | 
| <p>JET_errcatError 1</p> | <p>Catégorie de niveau supérieur (aucune erreur ne doit être de cette classe).</p> | <p>Consultez les constantes d’erreur spécifiques.</p> | 
| <p>JET_errcatOperation 2</p> | <p>Représente les erreurs qui peuvent se produire à tout moment en raison de conditions incontrôlables et qui sont souvent temporaires. Consultez les sous-catégories si elles sont spécifiées.</p> | <p>Réessayez et si l’erreur persiste, Informez l’opérateur.</p> | 
| <p>JET_errcatFatal 3</p> | <p>Représente des erreurs irrécupérables qui, lorsqu’elles se produisent, créent un risque que ESE ne puisse pas continuer en toute sécurité (souvent transactionnelle), et les données peuvent être endommagées.</p> | <p>Redémarrez l’instance ou le processus. Si le problème persiste, Informez l’opérateur.</p> | 
| <p>JET_errcatIO 4</p> | <p>Représente les erreurs d’e/s qui proviennent du système d’exploitation et qui sont hors du contrôle de ESE. Ce type d’erreur peut être temporaire.</p> | <p>Réessayez, et si l’erreur persiste, demandez à l’opérateur de vérifier le disque.</p> | 
| <p>JET_errcatResource 5</p> | <p>Représente une catégorie d’erreurs liées à des conditions de ressources insuffisantes.</p> | <p>Consultez sous-catégories.</p> | 
| <p>JET_errcatMemory 6</p> | <p>Représente une erreur provoquée par un manque de mémoire.</p> | <p>Réessayez au bout d’un certain temps, libérez de la mémoire ou quittez.</p> | 
| <p>JET_errcatQuota 7</p> | <p>Certaines ressources « spécialisées » se trouvent dans des pools d’une certaine taille, ce qui facilite la détection des fuites de ces ressources.</p> | <p>L’application doit <strong>déclarer ()</strong> pour détecter ces problèmes lors du développement. Toutefois, dans le code de vente au détail, l’application doit traiter ceci comme une erreur de mémoire.</p> | 
| <p>JET_errcatDisk 8</p> | <p>Représente une erreur provoquée par un manque d’espace disque.</p> | <p>Réessayez ultérieurement pour déterminer si de l’espace disque est disponible ou demandez à l’opérateur de libérer de l’espace disque.</p> | 
| <p>JET_errcatData 9</p> | <p>Représente une catégorie de niveau supérieur pour les erreurs liées aux données.</p> | <p>Consultez sous-catégories.</p> | 
| <p>JET_errcatCorruption 10</p> | <p>Représente un problème d’endommagement, qui est souvent permanent sans action corrective.</p> | <p>Restauration à partir d’une sauvegarde à l’aide de l’opération de réparation des utilitaires ESE (cette opération restaure uniquement les données qui sont conservées/perdues). En outre, lorsque la méthode Recovery (JetInit) est utilisée, la récupération peut être effectuée en autorisant la perte de données (pour plus d’informations, consultez <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatInconsistent 11</p> | <p>Représente une erreur dans laquelle la base de données et/ou les fichiers journaux sont dans un état incohérent et ne peuvent pas être conciliés. Cette erreur peut être due à une mauvaise administration de l’application/de l’administrateur.</p> | <p>Restaurez à partir d’une sauvegarde à l’aide de l’opération de réparation des utilitaires ESE (qui restaure uniquement les données qui sont conservées/perdues). En outre, dans le cas de l’opération de <strong>récupération (JetInit)</strong> , la récupération peut être effectuée en autorisant la perte de données (pour plus d’informations, consultez <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatFragmentation 12</p> | <p>Représente une classe d’erreurs dans laquelle une ressource interne persistante s’est exécutée.</p> | <p>Pour les erreurs de base de données, la défragmentation hors connexion permet de résoudre le problème. Pour les fichiers journaux, récupérez d’abord toutes les bases de données attachées à un arrêt correct, puis supprimez tous les fichiers journaux et le point de contrôle.</p> | 
| <p>JET_errcatApi 13</p> | <p>Consultez sous-catégories.</p> | <p>Consultez sous-catégories.</p> | 
| <p>JET_errcatUsage 14</p> | <p>Représente une erreur d’utilisation. Le code client n’a pas transmis les arguments corrects à l’API <strong>Jet</strong> . Cette erreur persiste avec une nouvelle tentative.</p> | <p>Le code client doit utiliser la méthode <strong>Assert ()</strong> pour s’assurer que cette classe d’erreurs n’est pas retournée, de sorte que les problèmes peuvent être détectés pendant le développement. Dans la version commerciale, l’application doit avertir l’opérateur de l’erreur.</p> | 
| <p>JET_errcatState 15</p> | <p>Représente une classe de messages que l’API peut retourner pour décrire l’état de la base de données. Par exemple, la méthode <a href="gg294103(v=exchg.10).md">JetSeek ()</a> peut retourner <strong>JET_errRecordNotFound</strong> lorsque l’enregistrement demandé est introuvable.</p> | <p>Varie en fonction de l’API.</p> | 
| <p>JET_errcatObsolete 16</p> | <p>Représente les erreurs qui proviennent d’une version antérieure du moteur. Ces erreurs ne doivent pas être retournées par le moteur actuel.</p> | <p>Inconnu.</p> | 
| <p>JET_errcatMax 17</p> | <p>Constante qui indique la fin de l’énumération.</p> | <p>N/A.</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows 8 Server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


