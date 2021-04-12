---
description: 'En savoir plus sur : énumération JET_ERRCAT'
title: Énumération JET_ERRCAT (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203146"
---
# <a name="jet_errcat-enumeration"></a>Énumération JET_ERRCAT

Catégorie d’erreur. La hiérarchie est la suivante : JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problèmes d’e/s incorrects, peuvent être temporaires ou non. | |--JET_errcatResource | |--JET_errcatMemory//mémoire insuffisante (toutes les variantes) | |--JET_errcatQuota | |--JET_errcatDisk//espace disque insuffisant (toutes les variantes) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//est généralement dû à une mauvaise utilisation de l’utilisateur | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>Membres

<table>
<thead>
<tr class="header">
<th></th>
<th>Nom du membre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Unknown</td>
<td>Catégorie inconnue.</td>
</tr>
<tr class="even">
<td></td>
<td>Error</td>
<td>Catégorie générique.</td>
</tr>
<tr class="odd">
<td></td>
<td>Opération</td>
<td>Erreurs qui peuvent généralement se produire à tout moment en raison de conditions incontrôlables. Souvent temporaire, mais pas toujours. Récupération : réessayez probablement ou Informez l’opérateur.</td>
</tr>
<tr class="even">
<td></td>
<td>Erreur irrécupérable</td>
<td>Cette erreur de tri se produit uniquement lorsque le moteur ESE rencontre une condition d’erreur trop grave, que nous ne pouvons pas continuer dans une méthode sécurisée (souvent transactionnelle) et plutôt que des données endommagées. nous générons des erreurs de cette catégorie. Récupération : redémarrez l’instance ou le processus. Si le problème persiste, Informez l’opérateur.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>O des erreurs proviennent du système d’exploitation et sont hors du contrôle ESE, ce type d’erreur est peut-être temporaire. Récupération : nouvelle tentative. Si elle n’est pas résolue, demandez à l’opérateur à propos du problème de disque.</td>
</tr>
<tr class="even">
<td></td>
<td>Ressource</td>
<td>Il s’agit d’une catégorie qui indique l’une des nombreuses conditions d’insuffisance de ressources potentielles.</td>
</tr>
<tr class="odd">
<td></td>
<td>Mémoire</td>
<td>Condition de mémoire insuffisante classique. Récupération : attendez un moment et réessayez, libérez de la mémoire ou quittez.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Certaines &quot; &quot; ressources spécialisées se trouvent dans des pools d’une certaine taille, ce qui facilite la détection des fuites de ces ressources. Récupération : peut nécessiter des modifications de code mineures. Votre application doit avoir une action de débogage uniquement, telle qu’une assertion, sur ces conditions afin de les détecter pendant le développement. Pour le code de vente au détail, nous vous recommandons de traiter cette erreur comme une erreur de catégorie mémoire et de réessayer, de libérer de la mémoire ou de quitter l’opération.</td>
</tr>
<tr class="odd">
<td></td>
<td>Disque</td>
<td>Conditions de disque insuffisant. Récupération : peut réessayer plus tard dans l’espoir que de l’espace est disponible, ou demander à l’opérateur de libérer de l’espace disque.</td>
</tr>
<tr class="even">
<td></td>
<td>Données</td>
<td>Erreur liée aux données.</td>
</tr>
<tr class="odd">
<td></td>
<td>Altération</td>
<td>Mon disque dur est à la maison. Problèmes d’altération classiques, souvent permanents sans action corrective. Récupération : restaurer à partir de la sauvegarde, peut-être l’opération de réparation des utilitaires ESE (qui ne restaure que les données qui sont conservées/perdues). En outre, dans le cas de la récupération (JetInit), il est possible d’effectuer une récupération en autorisant la perte de données.</td>
</tr>
<tr class="even">
<td></td>
<td>Incohérent</td>
<td>Cela est similaire à un endommagement dans le fait que la base de données et/ou les fichiers journaux sont dans un état incohérent et non réconciliable les uns avec les autres. Cela est souvent dû à une mauvaise gestion des applications/administrateurs. Récupération : restaurer à partir de la sauvegarde, peut-être l’opération de réparation des utilitaires ESE (qui ne restaure que les données qui sont conservées/perdues). En outre, dans le cas de la récupération (JetInit), il est possible d’effectuer une récupération en autorisant la perte de données.</td>
</tr>
<tr class="odd">
<td></td>
<td>Fragmentation</td>
<td>Il s’agit d’une classe d’erreurs dans laquelle certaines ressources internes persistantes ont été exécutées. Récupération : pour les erreurs de base de données, la défragmentation hors connexion permet de corriger le problème. pour les fichiers journaux, _commencez_ par récupérer toutes les bases de données attachées à un arrêt correct, puis supprimez tous les fichiers journaux et le point de contrôle.</td>
</tr>
<tr class="even">
<td></td>
<td>MobileVBActiveX</td>
<td>Conteneur pour l’utilisation et l’État.</td>
</tr>
<tr class="odd">
<td></td>
<td>Utilisation</td>
<td>Erreur d’utilisation classique, ce qui signifie que le code client n’a pas transmis d’arguments corrects à l’API JET. Cette erreur ne sera probablement pas déplacée avec une nouvelle tentative. Récupération : en général, le code client doit déclarer () que cette classe d’erreurs n’est pas retournée, de sorte que les problèmes peuvent être détectés pendant le développement. Dans la version commerciale, l’application aura probablement peu d’options, mais pour retourner le problème à l’opérateur.</td>
</tr>
<tr class="even">
<td></td>
<td>State</td>
<td>Il s’agit de la classification des différents signaux que l’API peut renvoyer décrivent l’état de la base de données, un cas classique est JET_errRecordNotFound qui peut être retourné par JetSeek () lorsque l’enregistrement que vous avez demandé n’a pas été trouvé. La récupération : pas vraiment pertinente, dépend beaucoup de l’API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Obsolète</td>
<td>L’erreur est reconnue comme une erreur valide, mais elle n’est pas censée être retournée par cette version de l’API.</td>
</tr>
<tr class="even">
<td></td>
<td>Max</td>
<td>Valeur maximale de l’énumération. Cela ne doit pas être utilisé.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
