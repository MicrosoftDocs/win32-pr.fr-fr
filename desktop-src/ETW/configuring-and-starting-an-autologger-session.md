---
description: La session de suivi d’événements autologger enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configuration et démarrage d’une session de journalisation automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102038"
---
# <a name="configuring-and-starting-an-autologger-session"></a>Configuration et démarrage d’une session de journalisation automatique

La session de suivi d’événements autologger enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation. Les applications et les pilotes de périphériques peuvent utiliser la session de journalisation automatique pour capturer des suivis avant que l’utilisateur se connecte. Notez que certains pilotes de périphérique, tels que les pilotes de périphériques de disque, ne sont pas chargés au moment du démarrage de la session de journalisation automatique.

L’enregistreur automatique diffère de l’enregistreur d’événements global des manières suivantes :

-   Vous pouvez spécifier une ou plusieurs sessions de journalisation automatique (le journal global était une session unique à laquelle tous les événements ont été consignés).
-   Le journal automatique envoie une notification d’activation aux fournisseurs au démarrage de la session (le journal global n’a pas envoyé de notification d’activation aux fournisseurs, de sorte que les fournisseurs devaient s’appuyer sur d’autres moyens pour savoir si la session de journalisation globale a été démarrée pour commencer à enregistrer des événements).
-   Le journal automatique ne prend pas en charge la journalisation des événements du journal de noyau NT (voir le membre **EnableFlags** des [**Propriétés de \_ suivi \_ d’événement**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Pour consigner les événements du journal de noyau NT, vous devez utiliser l’enregistreur d’événements [Global](configuring-and-starting-the-global-logger-session.md).

Pour plus d’informations sur la vue globale de l’enregistreur d’événements, consultez [configuration et démarrage de la session d’enregistreur](configuring-and-starting-the-global-logger-session.md)d’événements globale.

> [!Note]  
> ETW prend en charge le journal automatique sur Windows Vista et versions ultérieures. Utilisez l' [enregistreur](configuring-and-starting-the-global-logger-session.md) d’événements global sur les systèmes d’exploitation antérieurs.

 

Vous utilisez le registre pour configurer la session de journalisation automatique. Ajoutez la clé de Registre suivante, si elle n’est pas déjà présente :

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

Sous la clé de l' **enregistreur** automatique, créez une clé pour chaque session de journalisation automatique que vous souhaitez configurer, comme indiqué dans l’exemple suivant.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

Pour chaque session, créez une clé pour chaque fournisseur que vous souhaitez activer dans la session. Utilisez le GUID du fournisseur comme clé.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

Le tableau suivant décrit les valeurs que vous pouvez définir pour chaque session de journalisation automatique. Vous devez disposer de privilèges d’administrateur pour spécifier ces valeurs de registre. La valeur de **début** et de **GUID** sont les seules valeurs requises pour démarrer la session de journalisation automatique. toutes les autres valeurs ont des paramètres par défaut qui sont utilisés si la valeur n’est pas présente dans le registre. En règle générale, vous devez utiliser les valeurs par défaut. Si vous spécifiez une valeur que ETW ne peut pas prendre en charge, ETW remplace la valeur.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Taille de chaque mémoire tampon, en kilo-octets. Doit être inférieur à un mégaoctet. ETW utilise la taille de la mémoire physique pour calculer cette valeur.<br/></td>
</tr>
<tr class="even">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Minuteur à utiliser lors de la journalisation de l’horodatage pour chaque événement.
<ul>
<li>1 = valeur de compteur de performance (haute résolution)</li>
<li>2 = minuterie du système</li>
<li>3 = compteur du cycle de l’UC</li>
</ul>
Pour obtenir une description de chaque type d’horloge, consultez le membre <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> La valeur par défaut est 1 (valeur du compteur de performances) sur Windows Vista et versions ultérieures. Avant Windows Vista, la valeur par défaut est 2 (horloge système).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Pour désactiver la persistance en temps réel, définissez cette valeur sur 1. La valeur par défaut est 0 (activé) pour les sessions en temps réel.<br/> Si la persistance en temps réel est activée, les événements en temps réel qui n’ont pas été remis au moment de l’arrêt de l’ordinateur sont conservés. Les événements seront ensuite remis au consommateur la prochaine fois que le consommateur se connectera à la session. <br/></td>
</tr>
<tr class="even">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Ne définissez pas cette valeur ou modifiez-la. Cette valeur est le numéro de série utilisé pour incrémenter le nom du fichier journal si <strong>FileMax</strong> est spécifié. Si la valeur n’est pas valide, 1 est utilisé.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Chemin d’accès complet du fichier journal. Le chemin d’accès à ce fichier doit exister. Le fichier journal est un fichier journal séquentiel. Le chemin d’accès est limité à 1024 caractères.<br/> Si <strong>filename</strong> n’est pas spécifié, les événements sont écrits dans%SystemRoot%\System32\LogFiles\WMI \& lt ; NomSession &gt; . etl. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Nombre maximal d’instances du fichier journal créé par ETW. Si le fichier journal spécifié dans <strong>filename</strong> existe, ETW ajoute la valeur <strong>FileCounter</strong> au nom de fichier. Par exemple, si le nom du fichier journal par défaut est utilisé, le formulaire est%SystemRoot%\System32\LogFiles\WMI \& lt ; NomSession &gt; . etl. NNNN. <br/> Lors du premier démarrage de l’ordinateur, le nom de fichier est &lt; nom_session. &gt; ETL. 0001, la deuxième fois, le nom de fichier est &lt; nom_session &gt; . etl. 0002, et ainsi de suite. Si <strong>FileMax</strong> a la valeur 3, au quatrième redémarrage de l’ordinateur, ETW rétablit la valeur 1 pour le compteur et remplace &lt; NomSession &gt; . etl. 0001, le cas échéant.<br/> Le nombre maximal d’instances du fichier journal pris en charge est de 16.<br/> N’utilisez pas cette fonctionnalité avec le mode de fichier journal <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Fréquence, en secondes, de vidage forcé des mémoires tampons de trace. La durée de vidage minimale est de 1 seconde. Ce vidage forcé s’ajoute au vidage automatique qui se produit lorsqu’une mémoire tampon est saturée et lorsque la session de trace s’arrête. <br/> Dans le cas d’un enregistreur d’événements en temps réel, la valeur zéro (valeur par défaut) signifie que le temps de vidage sera défini sur 1 seconde. Un enregistreur d’événements en temps réel est lorsque <strong>LogFileMode</strong> a la valeur <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> La valeur par défaut est 0. Par défaut, les mémoires tampons sont vidées uniquement lorsqu’elles sont pleines. <br/></td>
</tr>
<tr class="even">
<td><strong>Uniques</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Chaîne qui contient un GUID qui identifie de façon unique la session. Cette valeur est requise.</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Spécifiez un ou plusieurs modes de journal. Pour connaître les valeurs possibles, consultez <a href="logging-mode-constants.md">constantes de mode de journalisation</a>. La valeur par défaut est <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. Au lieu d’écrire dans un fichier journal, vous pouvez spécifier <strong>EVENT_TRACE_BUFFERING_MODE</strong> ou <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> La spécification de <strong>EVENT_TRACE_BUFFERING_MODE</strong> permet d’éviter le coût de vidage du contenu de la session sur le disque lorsque le système de fichiers devient disponible. <br/> Notez que l’utilisation de <strong>EVENT_TRACE_BUFFERING_MODE</strong> amène le système à ignorer la valeur <strong>MaximumBuffers</strong> , car la taille de la mémoire tampon est à la place le produit de <strong>MinimumBuffers</strong> et <strong>bufferSize</strong>.<br/> Les sessions de journal automatique ne prennent pas en charge le mode de journalisation <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .<br/> Si <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> est spécifié, <strong>bufferSize</strong> doit être fourni explicitement et doit être le même dans l’enregistreur d’événements et le fichier ajouté.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Taille maximale du fichier journal, en mégaoctets. La session est fermée lorsque la taille maximale est atteinte, sauf si vous êtes en mode de fichier journal circulaire. Pour ne spécifier aucune limite, définissez la valeur sur 0. La valeur par défaut est 100 Mo, si elle n’est pas définie. Le comportement qui se produit lorsque la taille de fichier maximale est atteinte dépend de la valeur de <strong>LogFileMode</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Nombre maximal de mémoires tampons à allouer. En général, cette valeur est le nombre minimal de mémoires tampons plus vingt. ETW utilise la taille de la mémoire tampon et la taille de la mémoire physique pour calculer cette valeur. Cette valeur doit être supérieure ou égale à la valeur de <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Nombre minimal de mémoires tampons à allouer au démarrage. Le nombre minimal de mémoires tampons que vous pouvez spécifier est deux mémoires tampons par processeur. Par exemple, sur un ordinateur à processeur unique, le nombre minimal de mémoires tampons est de deux.<br/></td>
</tr>
<tr class="odd">
<td><strong>Start</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Pour que la session de journalisation automatique démarre lors du prochain redémarrage de l’ordinateur, définissez cette valeur sur 1 ; dans le cas contraire, définissez cette valeur sur 0.<br/></td>
</tr>
<tr class="even">
<td><strong>État</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>État de démarrage de l’enregistreur automatique. Si le journal automatique n’a pas pu démarrer, la valeur de cette clé est le code d’erreur Win32 approprié. Si le journal automatique a démarré, la valeur de cette clé est <strong>ERROR_SUCCESS</strong> (0).<br/></td>
</tr>
</tbody>
</table>



 

Le tableau suivant décrit les valeurs que vous pouvez définir pour chaque fournisseur que vous souhaitez activer pour votre session. Vous devez disposer de privilèges d’administrateur pour spécifier ces valeurs de registre. Si vous spécifiez une valeur que ETW ne peut pas prendre en charge, ETW remplace la valeur.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Activé</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Détermine si le fournisseur est activé. Pour activer le fournisseur, définissez cette valeur sur 1. Pour désactiver le fournisseur, définissez cette valeur sur 0. La valeur par défaut est 0.</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valeur définie par le fournisseur qui spécifie la classe des événements pour lesquels le fournisseur génère des événements. Pour plus d’informations, consultez le paramètre <em>EnableFlags</em> de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> . Spécifiez ce nom de valeur si le fournisseur ne prend pas en charge <strong>MatchAnyKeyword</strong> ou <strong>MatchAllKeyword</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valeur définie par le fournisseur qui spécifie le niveau de détail inclus dans l’événement. Par exemple, vous pouvez utiliser cette valeur pour indiquer le niveau de gravité des événements générés par le fournisseur (informations, avertissement, erreur). Pour obtenir la liste des niveaux prédéfinis, consultez le paramètre <em>Level</em> de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Utilisez cette valeur pour inclure un ou plusieurs des éléments suivants dans le fichier journal :
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = inclure dans les données étendues l’identificateur de sécurité (SID) de l’utilisateur.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = include dans les données étendues identificateur de session Terminal Server.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = inclure dans les données étendues trace de la pile des appels pour les événements écrits à l’aide de <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtre tous les événements qui n’ont pas de mot clé non nul spécifié.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indique que cet appel à <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> doit activer un <a href="provider-traits.md">groupe de fournisseurs</a> plutôt qu’un fournisseur d’événements individuel.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = inclure la clé de début du processus dans les données étendues.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = inclure la clé d’événement dans les données étendues.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtre tous les événements qui sont marqués comme un événement non privé ou qui proviennent d’un processus qui est marqué comme non privé.</li>
</ul>
Pour plus d’informations sur ces éléments, consultez le <strong>EnableProperty</strong> de la structure <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Masque de réécriture des mots clés qui déterminent la catégorie d’événements que le fournisseur doit écrire. Le fournisseur écrit l’événement si l’un des bits de mot clé de l’événement correspond à l’un des bits définis dans ce masque. Pour spécifier que le fournisseur doit écrire tous les événements, définissez cette valeur sur zéro. Pour obtenir un exemple, consultez la section Notes de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Ce masque de masque est facultatif. Ce masque limite davantage la catégorie d’événements que vous souhaitez que le fournisseur écrive. Si le mot clé de l’événement répond à la condition <em>MatchAnyKeyword</em> , le fournisseur écrit l’événement uniquement si tous les bits de ce masque existent dans le mot clé de l’événement. Ce masque n’est pas utilisé si <em>MatchAnyKeyword</em> est égal à zéro. Pour obtenir un exemple, consultez la section Notes de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
</tbody>
</table>



 

Une fois le registre modifié, la session de journalisation automatique est lancée lors du prochain redémarrage de l’ordinateur. La session de journalisation automatique appelle la fonction [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) pour activer les fournisseurs.

Les sessions de l’enregistreur d’événements automatique augmentent le temps de démarrage du système et doivent être utilisées avec modération. Les services qui souhaitent capturer des informations pendant le processus de démarrage doivent envisager d’ajouter la logique du contrôleur à lui-même au lieu d’utiliser la session de journalisation automatique.

Pour arrêter une session de journalisation automatique, appelez la fonction [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) . Le nom de session que vous transmettez à la fonction est le nom de la clé de registre que vous avez utilisée pour définir la session dans le registre.

Sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures, la charge utile d’événement, la portée et les filtres de parcours de pile peuvent être utilisés par la fonction [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) et les structures de [**\_ \_ descripteur de filtre d’événement**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) et de [**\_ \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) pour filtrer sur des conditions spécifiques dans une session de journalisation. Pour plus d’informations sur les filtres de charge utile d’événement, consultez les fonctions [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)et [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , ainsi que les structures de prédicat **activer les \_ \_ paramètres de trace**, **\_ \_ descripteur de filtre d’événement** et de [**\_ filtre \_ de charge utile**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .

Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

Pour plus d’informations sur le démarrage d’une session privée de journalisation, consultez [configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md).

Pour plus d’informations sur le démarrage d’une session de journal de noyau NT, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**ACTIVER \_ les \_ paramètres de trace**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**descripteur de filtre d’événements \_ \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_prédicat de filtre de charge utile \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Mise à jour d’une session de suivi d’événements](updating-an-event-tracing-session.md)
</dt> </dl>
