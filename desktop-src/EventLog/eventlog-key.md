---
description: 'Le journal des événements contient les journaux standard et les journaux personnalisés suivants :'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Clé EventLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eed1e64d3084d6b952693957c65766b257cb552a861c9989ea0550111e9b224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383769"
---
# <a name="eventlog-key"></a>Clé EventLog

Le journal des événements contient les journaux standard et les journaux personnalisés suivants :



| Journal             | Description                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Application** | Contient les événements journalisés par les applications. Par exemple, une application de base de données peut enregistrer une erreur de fichier. Le développeur de l’application décide des événements à enregistrer.                                                                             |
| **Sécurité**    | Contient des événements tels que des tentatives de connexion valides et non valides, ainsi que des événements liés à l’utilisation des ressources telles que la création, l’ouverture ou la suppression de fichiers ou d’autres objets. Un administrateur peut démarrer l’audit pour enregistrer les événements dans le journal de sécurité. |
| **Système**      | Contient les événements consignés par les composants du système, tels que l’échec du chargement d’un pilote ou d’un autre composant système au démarrage.                                                                                                               |
| *CustomLog*     | Contient les événements journalisés par les applications qui créent un journal personnalisé. L’utilisation d’un journal personnalisé permet à une application de contrôler la taille du journal ou d’attacher des listes de contrôle d’accès (ACL) à des fins de sécurité sans affecter d’autres applications.                         |



 

Le service de journalisation des événements utilise les informations stockées dans la clé de Registre **EventLog** . La clé **EventLog** contient plusieurs sous-clés, appelées *journaux*. Chaque journal contient des informations que le service de journalisation des événements utilise pour localiser des ressources quand une application écrit dans le journal des événements et les lit.

La structure de la clé **EventLog** est la suivante :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

Notez que les contrôleurs de domaine enregistrent les événements dans les journaux du service d' **Annuaire** et du **service de réplication de fichiers** et les événements d’enregistrement dans le **serveur DNS**.

Chaque journal peut contenir les valeurs de Registre suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur de Registre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>En douane</strong></td>
<td>Restreint l’accès au journal des événements. Cette valeur est de type REG_SZ. Le format utilisé est le langage SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> ). Construisez une liste de contrôle d’accès qui accorde un ou plusieurs des droits suivants :<dl> Clear (0x0004)<br />
Lecture (0x0001)<br />
Écriture (0x0002)<br />
</dl> Pour être un SDDL syntaxiquement valide, la valeur de douane doit spécifier un propriétaire et un propriétaire de groupe (par exemple, O :BAG : SY), mais le propriétaire et le propriétaire du groupe ne sont pas utilisés. Si la valeur de douane est incorrecte, un événement est déclenché dans le journal des événements système au démarrage du service du journal des événements, et le journal des événements obtient un descripteur de sécurité par défaut qui est identique à la valeur d’origine de la douane du journal des applications. Les listes SACL ne sont pas prises en charge.<br/> Pour plus d’informations, consultez sécurité de la <a href="event-logging-security.md">journalisation des événements</a>.<br/> <strong>Windows Server 2003 :</strong> Les listes SACL sont prises en charge.<br/> <strong>Windows XP/2000 :</strong> Cette valeur n’est pas prise en charge.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>DisplayNameFile</strong></td>
<td>Cette valeur n'est pas utilisée. <strong>Windows Server 2003 et Windows XP/2000 :</strong> Nom du fichier qui stocke le nom localisé du journal des événements. Le nom stocké dans ce fichier apparaît en tant que nom de journal dans observateur d’événements. Si cette entrée n’apparaît pas dans le registre pour un journal des événements, observateur d’événements affiche le nom de la sous-clé du Registre comme nom de journal. Cette valeur est de type REG_EXPAND_SZ. La valeur par défaut est% SystemRoot% \system32\els.dll.<br/></td>
</tr>
<tr class="odd">
<td><strong>DisplayNameID</strong></td>
<td>Cette valeur n'est pas utilisée. <strong>Windows Server 2003 et Windows XP/2000 :</strong> Numéro d’identification du message de la chaîne de nom de journal. Ce nombre indique le message dans lequel s’affiche le nom complet localisé. Le message est stocké dans le fichier spécifié par la valeur <strong>DisplayNameFile</strong> . Cette valeur est de type REG_DWORD.<br/></td>
</tr>
<tr class="even">
<td><strong>File</strong></td>
<td>Chemin d’accès complet au fichier dans lequel chaque journal des événements est stocké. Cela permet à observateur d’événements et à d’autres applications de rechercher les fichiers journaux. Cette valeur est de type REG_SZ ou REG_EXPAND_SZ. Cette valeur est facultative. Si la valeur n’est pas spécifiée, la valeur par défaut est%SystemRoot%\system32\winevt\logs\ suivie d’un nom de fichier basé sur le nom de la clé de Registre du journal des événements. Le chemin d’accès au fichier journal des événements spécifique doit être défini à l’aide de l’utilitaire de ligne de commande wevtutil.exe ou à l’aide de la fonction <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> avec EvtChannelLoggingConfigLogFilePath passé dans le paramètre <em>PropertyId</em> .<br/> Si un fichier spécifique est défini, assurez-vous que le service journal des événements dispose des autorisations complètes sur le fichier.<br/> Cette valeur doit être un nom de fichier valide pour un fichier situé dans un répertoire local (et non un ordinateur distant, et non un périphérique DOS, et non une disquette, et non un canal). Si le paramètre du fichier est incorrect, un événement est déclenché dans le journal des événements système au démarrage du service journal des événements.<br/> N’utilisez pas de variables d’environnement, dans le chemin d’accès au fichier, qui ne peuvent pas être développées dans le contexte du service journal des événements.<br/> <strong>Windows Server 2003 et Windows XP/2000 :</strong> La valeur par défaut est%SystemRoot%\system32\config\ suivie d’un nom de fichier basé sur le nom de la clé de Registre du journal des événements. Si le paramètre de fichier est défini sur une valeur non valide, le journal n’est pas correctement initialisé, ou toutes les demandes sont dirigées en mode silencieux vers le journal par défaut (application).<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxSize</strong></td>
<td>Taille maximale, en octets, du fichier journal. Cette valeur est de type REG_DWORD. La valeur doit être un multiple de 64 Ko pour un système, une application ou un journal de sécurité. La valeur par défaut est 1 Mo. <strong>Windows Server 2003 et Windows XP/2000 :</strong> La valeur est limitée à 0xFFFFFFFF, et la valeur par défaut est 512 Ko.<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>Cette valeur n’est pas utilisée. <strong>Windows Server 2003 et Windows XP/2000 :</strong> Cette valeur est le nom de la sous-clé qui contient les valeurs par défaut des entrées de la sous-clé pour la source de l’événement. Cette valeur est de type REG_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>Rétention</strong></td>
<td>Cette valeur est de type REG_DWORD. La valeur par défaut est 0. Si cette valeur est 0, les enregistrements des événements sont toujours remplacés. Si cette valeur est 0xFFFFFFFF ou toute valeur différente de zéro, les enregistrements ne sont jamais remplacés. Lorsque le fichier journal atteint sa taille maximale, vous devez effacer le journal manuellement. dans le cas contraire, les nouveaux événements sont ignorés. Vous devez également effacer le journal avant de pouvoir modifier sa taille. <strong>Windows Server 2003 et Windows XP/2000 :</strong> Cette valeur correspond à l’intervalle de temps, en secondes, pendant lequel les enregistrements des événements sont protégés contre le remplacement. Lorsque l’âge d’un événement atteint ou dépasse cette valeur, il peut être remplacé.<br/></td>
</tr>
<tr class="even">
<td><strong>Sources</strong></td>
<td>Cette valeur n'est pas utilisée. <strong>Windows Server 2003 et Windows XP/2000 :</strong> Noms des applications, des services ou des groupes d’applications qui écrivent des événements dans ce journal. Cette valeur doit être lue et non modifiée. Le service journal des événements gère la liste en fonction de chaque programme répertorié dans une sous-clé sous le journal. Cette valeur est de type REG_MULTI_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>Cette valeur est de type REG_DWORD, et est utilisée par le service journal des événements pour déterminer si un journal des événements doit être enregistré automatiquement. La valeur par défaut est 0, ce qui désactive la sauvegarde automatique. Le service sauvegarde le fichier journal uniquement si la valeur de rétention est-1 (0xFFFFFFFF). Les autres valeurs sont ignorées. <strong>Windows Server 2003 :</strong> La rétention peut être définie sur-1 (0xFFFFFFFF) ou 1 (0x00000001) pour que AutoBackupLogFiles fonctionne. Les autres valeurs sont ignorées.<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>Cette valeur n'est pas utilisée. <strong>Windows XP/2000 :</strong> Cette valeur est de type REG_DWORD, et la valeur par défaut est 1. Lorsque la valeur est définie sur 1, elle restreint l’accès du compte invité et anonyme au journal des événements, et lorsque cette valeur est 0, elle autorise l’accès du compte invité au journal des événements.<br/></td>
</tr>
<tr class="odd">
<td><strong>Isolement</strong></td>
<td>Définit les autorisations d’accès par défaut pour le journal. Cette valeur est de type REG_SZ. Vous pouvez spécifier l'une des valeurs suivantes :
<ul>
<li><strong>Application</strong></li>
<li><strong>Système</strong></li>
<li><strong>Personnalisée</strong></li>
</ul>
L’isolation par défaut est <strong>application</strong>. Les autorisations par défaut pour l' <strong>application</strong> sont (illustrées à l’aide de SDDL) : <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
Les autorisations par défaut pour <strong>System</strong> sont (illustrées à l’aide de SDDL) : <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre>
Les autorisations par défaut pour l’isolation <strong>personnalisée</strong> sont les mêmes que celles de l’application.<br/> <strong>Windows Server 2003 et Windows XP/2000 :</strong> Cette valeur n’est pas disponible.<br/></td>
</tr>
</tbody>
</table>



 

Chaque journal contient également des sources d’événements. Pour plus d’informations, consultez [sources d’événements](event-sources.md).

