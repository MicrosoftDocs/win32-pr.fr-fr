---
description: 'En savoir plus sur : JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523240"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_errcat"></a>JET_ERRCAT

Le **JET_ERRCAT** groupe de constantes décrit les classifications ou les catégories d’erreurs de niveau supérieur. Ce groupe de constantes permet aux applications de définir le traitement par défaut pour une classification des erreurs, au lieu de gérer chaque cas d’erreur individuellement. Elle garantit également que l’application n’a pas à gérer les nouvelles conditions d’erreur incluses dans les classifications existantes.

Remarque : cette documentation est basée sur une version préliminaire du moteur de stockage extensible. Ces informations sont susceptibles d’être modifiées.

Les constantes de **JET_ERRCAT** sont organisées dans une hiérarchie spécifique de conditions et de sous-conditions, comme suit :

| Erreur---| opération de---(Al) | |---irrécupérable | |---e/s | |---ressource | |---de la mémoire | |---quota | |---disque | |---des données | |---de l’altération | |---incohérent | |---de la fragmentation | |---l’API | utilisation de---

Le tableau suivant répertorie les constantes d' **JET_ERRCAT** et fournit une description et des informations de récupération, le cas échéant.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valeur</p></th>
<th><p>Description</p></th>
<th><p>Récupération</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errcatUnknown 0</p></td>
<td><p>Catégorie d’erreur non valide.</p></td>
<td><p>N/A.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>Catégorie de niveau supérieur (aucune erreur ne doit être de cette classe).</p></td>
<td><p>Consultez les constantes d’erreur spécifiques.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Représente les erreurs qui peuvent se produire à tout moment en raison de conditions incontrôlables et qui sont souvent temporaires. Consultez les sous-catégories si elles sont spécifiées.</p></td>
<td><p>Réessayez et si l’erreur persiste, Informez l’opérateur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Représente des erreurs irrécupérables qui, lorsqu’elles se produisent, créent un risque que ESE ne puisse pas continuer en toute sécurité (souvent transactionnelle), et les données peuvent être endommagées.</p></td>
<td><p>Redémarrez l’instance ou le processus. Si le problème persiste, Informez l’opérateur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Représente les erreurs d’e/s qui proviennent du système d’exploitation et qui sont hors du contrôle de ESE. Ce type d’erreur peut être temporaire.</p></td>
<td><p>Réessayez, et si l’erreur persiste, demandez à l’opérateur de vérifier le disque.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Représente une catégorie d’erreurs liées à des conditions de ressources insuffisantes.</p></td>
<td><p>Consultez sous-catégories.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Représente une erreur provoquée par un manque de mémoire.</p></td>
<td><p>Réessayez au bout d’un certain temps, libérez de la mémoire ou quittez.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Certaines &quot; &quot; ressources spécialisées se trouvent dans des pools d’une certaine taille, ce qui facilite la détection des fuites de ces ressources.</p></td>
<td><p>L’application doit <strong>déclarer ()</strong> pour détecter ces problèmes lors du développement. Toutefois, dans le code de vente au détail, l’application doit traiter ceci comme une erreur de mémoire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Représente une erreur provoquée par un manque d’espace disque.</p></td>
<td><p>Réessayez ultérieurement pour déterminer si de l’espace disque est disponible ou demandez à l’opérateur de libérer de l’espace disque.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Représente une catégorie de niveau supérieur pour les erreurs liées aux données.</p></td>
<td><p>Consultez sous-catégories.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Représente un problème d’endommagement, qui est souvent permanent sans action corrective.</p></td>
<td><p>Restauration à partir d’une sauvegarde à l’aide de l’opération de réparation des utilitaires ESE (cette opération restaure uniquement les données qui sont conservées/perdues). En outre, lorsque la méthode Recovery (JetInit) est utilisée, la récupération peut être effectuée en autorisant la perte de données (pour plus d’informations, consultez <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Représente une erreur dans laquelle la base de données et/ou les fichiers journaux sont dans un état incohérent et ne peuvent pas être conciliés. Cette erreur peut être due à une mauvaise administration de l’application/de l’administrateur.</p></td>
<td><p>Restaurez à partir d’une sauvegarde à l’aide de l’opération de réparation des utilitaires ESE (qui restaure uniquement les données qui sont conservées/perdues). En outre, dans le cas de l’opération de <strong>récupération (JetInit)</strong> , la récupération peut être effectuée en autorisant la perte de données (pour plus d’informations, consultez <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Représente une classe d’erreurs dans laquelle une ressource interne persistante s’est exécutée.</p></td>
<td><p>Pour les erreurs de base de données, la défragmentation hors connexion permet de résoudre le problème. Pour les fichiers journaux, récupérez d’abord toutes les bases de données attachées à un arrêt correct, puis supprimez tous les fichiers journaux et le point de contrôle.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Consultez sous-catégories.</p></td>
<td><p>Consultez sous-catégories.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Représente une erreur d’utilisation. Le code client n’a pas transmis les arguments corrects à l’API <strong>Jet</strong> . Cette erreur persiste avec une nouvelle tentative.</p></td>
<td><p>Le code client doit utiliser la méthode <strong>Assert ()</strong> pour s’assurer que cette classe d’erreurs n’est pas retournée, de sorte que les problèmes peuvent être détectés pendant le développement. Dans la version commerciale, l’application doit avertir l’opérateur de l’erreur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Représente une classe de messages que l’API peut retourner pour décrire l’état de la base de données. Par exemple, la méthode <a href="gg294103(v=exchg.10).md">JetSeek ()</a> peut retourner <strong>JET_errRecordNotFound</strong> lorsque l’enregistrement demandé est introuvable.</p></td>
<td><p>Varie en fonction de l’API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Représente les erreurs qui proviennent d’une version antérieure du moteur. Ces erreurs ne doivent pas être retournées par le moteur actuel.</p></td>
<td><p>Inconnu.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Constante qui indique la fin de l’énumération.</p></td>
<td><p>N/A.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Requiert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Nécessite Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>

