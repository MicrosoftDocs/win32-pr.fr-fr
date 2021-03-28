---
description: Les constantes suivantes représentent les modes de journalisation possibles pour une session de suivi d’événements.
ms.assetid: d12aaecb-776a-4476-9ba4-16af30fde9c2
title: Constantes de mode de journalisation
ms.topic: article
ms.date: 06/03/2020
ms.openlocfilehash: daa0233346718040653edbc75a10615f9fd31765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972286"
---
# <a name="logging-mode-constants"></a>Constantes de mode de journalisation

Les constantes suivantes représentent les modes de journalisation possibles pour une session de suivi d’événements.

Les constantes sont utilisées dans les membres **LogFileMode** du [**\_ \_ fichier journal de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea), des [**\_ \_ Propriétés de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) et des structures d' [**\_ \_ en-tête de fichier journal de trace**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header) . Ces constantes sont définies dans le fichier d’en-tête *Evntrace. h* .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NONE</strong> (0x00000000)</td>
<td>Identique à <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> sans aucune taille de fichier maximale spécifiée.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> (0x00000001)</td>
<td>Écrit les événements dans un fichier journal de façon séquentielle ; s’arrête lorsque le fichier atteint sa taille maximale. Ne pas utiliser avec <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> ou <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> (0x00000002)</td>
<td>Écrit des événements dans un fichier journal. Une fois que le fichier atteint la taille maximale, les événements les plus anciens sont remplacés par les événements entrants. Notez que le contenu du fichier journal circulaire peut apparaître dans le désordre sur les ordinateurs multiprocesseurs.<br/> N’utilisez pas with <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>ou <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_APPEND</strong> (0x00000004)</td>
<td>Ajoute des événements à un fichier journal séquentiel existant. Si le fichier n’existe pas, il est créé. À utiliser uniquement si vous spécifiez l' <a href="wnode-header.md"><strong>heure système</strong></a> pour la résolution de l’horloge, sinon, <a href="/windows/win32/api/evntrace/nf-evntrace-processtrace"><strong>ProcessTrace</strong></a> retourne les événements avec des horodatages incorrects. Lorsque vous utilisez <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, les valeurs de <strong>bufferSize</strong>, <strong>NumberOfProcessors</strong>et <strong>ClockType</strong> doivent être explicitement fournies et doivent être les mêmes dans le journal et le fichier ajouté.<br/> N’utilisez pas with <strong>EVENT_TRACE_REAL_TIME_MODE</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>ou <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>.<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> (0x00000008)</td>
<td>Bascule automatiquement vers un nouveau fichier journal lorsque le fichier atteint la taille maximale. Le membre <strong>maximumFileSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a> doit être défini. Le nom de fichier spécifié doit être une chaîne mise en forme (par exemple, la chaîne contient un% d, tel que c:\test%d.ETL). Chaque fois qu’un nouveau fichier est créé, un compteur est incrémenté et sa valeur est utilisée, la chaîne mise en forme est mise à jour et la chaîne résultante est utilisée comme nom de fichier.<br/> Cette option n’est pas autorisée pour les sessions de suivi d’événements privées et ne doit pas être utilisée pour les sessions de journalisation du noyau NT.<br/> N’utilisez pas with <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> ou <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_PREALLOCATE</strong>(0x00000020)</td>
<td>Réserve <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a> octets d’espace disque pour le fichier journal à l’avance. Le fichier occupe tout l’espace pendant la journalisation, pour les fichiers journaux circulaires et séquentiels. Lorsque vous arrêtez la session, le fichier journal est réduit à la taille nécessaire. Vous devez définir <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a>.<br/> Vous ne pouvez pas utiliser le mode pour les sessions de suivi d’événements privées.<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NONSTOPPABLE_MODE</strong>(0x00000040)</td>
<td>Impossible d’arrêter la session de journalisation. Ce mode est pris en charge uniquement par l’enregistreur automatique. cette option est prise en charge sur Windows Vista et versions ultérieures.<br/>.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_SECURE_MODE</strong> (0X00000080)</td>
<td>Limite les personnes autorisées à consigner les événements dans la session à ceux qui disposent de l’autorisation <a href="/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol"><strong>TRACELOG_LOG_EVENT</strong></a> . Cette option est prise en charge sur Windows Vista et versions ultérieures.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_REAL_TIME_MODE</strong> (0x00000100)</td>
<td>Remet les événements aux consommateurs en temps réel. Les événements sont remis lorsque les mémoires tampons sont vidées, et non au moment où le fournisseur écrit l’événement. Vous ne devez pas activer le mode en temps réel s’il n’y a pas de consommateurs pour consommer les événements, car les appels aux événements de journal finissent par échouer lorsque les mémoires tampons seront saturées. Avant Windows Vista, si les événements n’étaient pas consommés, les événements étaient ignorés. Ne spécifiez pas plusieurs consommateurs en temps réel dans un processus sur Windows XP intégral Server 2003. Au lieu de cela, il faut que l’un des threads consomme les événements et les distribue aux autres.<br/> <strong>Avant Windows Vista :</strong> Vous ne devez pas utiliser le mode temps réel, car le taux d’événements pris en charge est bien plus faible que la lecture du fichier journal (les événements peuvent être supprimés). En outre, l’ordre des événements n’est pas garanti sur les ordinateurs avec plusieurs processeurs. Le mode en temps réel est plus approprié pour les événements de type notification à faible trafic.<br/> <br/> Vous pouvez combiner ce mode avec d’autres modes de fichier journal ; Toutefois, n’utilisez pas ce mode avec EVENT_TRACE_PRIVATE_LOGGER_MODE. Notez que si vous combinez ce mode avec d’autres modes de fichier journal, les mémoires tampons sont vidées une fois par seconde, ce qui entraîne l’écriture de mémoires tampons partiellement remplies dans votre fichier journal. Par exemple, si vous utilisez des mémoires tampons de 64 Ko et que votre taux de journalisation est 1 événement chaque seconde, le service écrit 64 Ko/seconde dans votre fichier journal.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_DELAY_OPEN_FILE_MODE</strong>(0x00000200)</td>
<td>Ce mode permet de différer l’ouverture du fichier journal jusqu’à ce qu’un événement se produise. <br/>
<blockquote>
<strong>Remarque :</strong><br />
Sur Windows Vista ou version ultérieure, ce mode ne doit pas être appliqué.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_BUFFERING_MODE</strong> (0x00000400)</td>
<td>Ce mode écrit des événements dans une mémoire tampon circulaire. Les événements écrits au-delà de la taille totale de la mémoire tampon suppriment les événements les plus anciens encore dans la mémoire tampon. La taille de cette mémoire tampon est le produit de <strong>MinimumBuffers</strong> et <strong>BufferSize</strong> (voir <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>). À la suite de cette formule, toute mémoire tampon qui utilise <strong>EVENT_TRACE_BUFFERING_MODE</strong> ignore la valeur <strong>MaximumBuffers</strong> .<br/> Les événements ne sont pas écrits dans un fichier journal ou ne sont pas fournis en temps réel, et ETW ne vide pas les mémoires tampons. Pour obtenir un instantané de la mémoire tampon, appelez la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-flushtracea"><strong>FlushTrace</strong></a> .<br/> Ce mode est particulièrement utile pour déboguer des pilotes de périphérique avec la possibilité d’afficher le contenu de mémoires tampons en mémoire avec l’extension de débogueur de noyau <a href="/windows-hardware/drivers/devtest/trace-session">WMITrace</a> .<br/> N’utilisez pas with <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>ou <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> (0x00000800)</td>
<td>Crée une session de suivi d’événements en mode utilisateur qui s’exécute dans le même processus que son fournisseur de suivi d’événements. La mémoire pour les mémoires tampons provient de la mémoire du processus. Les processus qui ne nécessitent pas de données du noyau peuvent éliminer la surcharge associée aux transitions en mode noyau à l’aide d’une session de suivi d’événement privée.<br/> Si le fournisseur est inscrit par plusieurs processus, ETW ajoute l’identificateur de processus au nom du fichier journal pour créer un nom de fichier journal unique. Par exemple, si le contrôleur spécifie les noms des fichiers journaux en tant que c:\mylogs\myprivatelog.etl, ETW crée le fichier journal en tant que c:\mylogs\ myprivatelog.etl_nnnn, où nnnn est l’identificateur du processus. L’identificateur de processus n’est pas ajouté au premier processus qui inscrit le fournisseur, il est ajouté uniquement aux processus suivants qui inscrivent le fournisseur.<br/> Les sessions de suivi des événements privés présentent les limitations suivantes :<br/>
<ul>
<li>Une session privée peut enregistrer des événements uniquement pour les threads du processus dans lequel elle s’exécute.</li>
<li>Il peut y avoir jusqu’à huit sessions privées par processus.</li>
<li>Les sessions privées ne peuvent pas être utilisées avec la remise en temps réel.</li>
<li>Les événements qui sont générés par une session privée n’incluent pas le temps d’exécution pour les instructions en mode noyau ou en mode utilisateur, ni les détails au niveau du thread du temps processeur utilisé.</li>
</ul>
Les filtres d’ID de processus et les filtres de nom d’exécutable peuvent désormais être passés dans les API de contrôle de session lorsque les enregistreurs privés du système sont démarrés. Pour obtenir les meilleurs résultats dans les scénarios inter-processus, les mêmes filtres doivent être passés à chaque opération de contrôle pendant la session, y compris les appels Enable/diasble du fournisseur. Notez que les filtres ont le même format que ceux utilisés par <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a>. <br/> Vous pouvez utiliser ce mode conjointement avec le mode <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> .<br/> <strong>Avant Windows 10, version 1703 :</strong> Seul LocalSystem, l’administrateur et les utilisateurs du groupe d’administrateurs qui s’exécutent dans un processus avec élévation de privilèges peuvent créer une session privée. Si vous incluez l’indicateur <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> , n’importe quel utilisateur peut créer une session privée in-process. De plus, dans les versions antérieures de Windows, il ne peut y avoir qu’une seule session privée par processus (sauf si le mode de EVENT_TRACE_PRIVATE_IN_PROC est également spécifié, auquel cas vous pouvez créer jusqu’à trois sessions privées in-process). <br/> <strong>Avant Windows Vista :</strong> Les utilisateurs du groupe utilisateurs du journal des performances peuvent également créer une session privée.<br/> <br/> Ne pas utiliser avec EVENT_TRACE_REAL_TIME_MODE.<br/> <strong>Avant Windows 7 et Windows Server 2008 R2 :</strong> Ne pas utiliser avec EVENT_TRACE_FILE_MODE_NEWFILE.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_ADD_HEADER_MODE</strong>(0x00001000)</td>
<td>Cette option ajoute un en-tête au fichier journal.<br/>
<blockquote>
<strong>Remarque :</strong><br />
Sur Windows Vista ou version ultérieure, ce mode ne doit pas être appliqué.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_KBYTES_FOR_SIZE</strong>(0x00002000)</td>
<td>Utilisez kilo-octets comme unité de mesure pour spécifier la taille d’un fichier. L’unité de mesure par défaut est en mégaoctets. Ce mode s’applique à la valeur de Registre <strong>MaxFileSize</strong> pour une session de <a href="configuring-and-starting-an-autologger-session.md">journalisation</a> automatique et le membre <strong>maximumFileSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>. Cette option est prise en charge sur Windows Vista et versions ultérieures.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong>(0x00004000)</td>
<td>Utilise des numéros de séquence qui sont uniques dans les sessions de suivi d’événements. Ce mode s’applique uniquement aux événements journalisés à l’aide de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Pour plus d’informations, consultez <strong>TraceMessage</strong> pour plus d’informations sur l’utilisation.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> et <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> s’excluent mutuellement.<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> (0x00008000)</td>
<td>Utilise des numéros de séquence qui sont uniques uniquement pour une session de suivi d’événements individuelle. Ce mode s’applique uniquement aux événements journalisés à l’aide de la fonction <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Pour plus d’informations, consultez <strong>TraceMessage</strong> pour plus d’informations sur l’utilisation.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> et <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> s’excluent mutuellement.<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_RELOG_MODE</strong> (0x00010000)</td>
<td>Journalise l’événement sans inclure de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_header"><strong>EVENT_TRACE_HEADER</strong></a>.
<blockquote>
<strong>Remarque :</strong><br />
Ce mode ne doit pas être utilisé. Elle est réservée à un usage interne.
</blockquote>
<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> (0x00020000)</td>
<td>Utilisez conjointement avec le mode <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> pour démarrer une session privée. Ce mode impose que seul le processus qui a inscrit le GUID du fournisseur puisse démarrer la session de journalisation avec ce GUID.<br/> Vous pouvez créer jusqu’à trois sessions privées in-process par processus.<br/> Cette option est prise en charge sur Windows Vista et versions ultérieures.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_MODE_RESERVED</strong>(0x00100000)</td>
<td>Cette option est utilisée pour signaler le suivi des sections critiques et du tas. Cette option est prise en charge sur Windows Vista et versions ultérieures.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong>(0x00400000)</td>
<td>Cette option arrête la journalisation de l’arrêt hybride. Si ni <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> ni <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> n’est spécifié, ETW choisit une valeur par défaut selon que l’appelant provient de la session 0 ou non. Cette option est prise en charge sur Windows 8 et Windows Server 2012. <br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong>(0x00800000)</td>
<td>Cette option poursuit la journalisation de l’arrêt hybride. Si ni <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> ni <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> n’est spécifié, ETW choisit une valeur par défaut selon que l’appelant provient de la session 0 ou non. Cette option est prise en charge sur Windows 8 et Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_PAGED_MEMORY</strong> (0x01000000)</td>
<td>Utilise la mémoire paginée. Ce paramètre est recommandé afin que les événements n’utilisent pas la mémoire non paginée. Les mémoires tampons non paginées utilisent la mémoire non paginée pour l’espace de la mémoire tampon. Étant donné que les mémoires tampons non paginées ne sont jamais paginées, une session de journalisation s’effectue correctement. L’utilisation de mémoires tampons paginables est moins gourmande en ressources.<br/> Les fournisseurs en mode noyau et les journaux système ne peuvent pas consigner des événements dans des sessions qui spécifient ce mode de journalisation.<br/> Ce mode est ignoré si <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> est défini.<br/> Vous ne pouvez pas utiliser ce mode avec l’enregistreur d’événements de noyau NT.<br/> <strong>Windows 2000 :</strong> Cette valeur n’est pas prise en charge.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_SYSTEM_LOGGER_MODE</strong>(0x02000000)</td>
<td>Cette option reçoit les événements de SystemTraceProvider. Si le paramètre de<em>Propriétés</em> <a href="/windows/win32/api/evntrace/nf-evntrace-starttracea"><strong>StartTrace</strong></a> <strong>LogFileMode</strong> comprend cet indicateur, l’enregistreur d’événements est un journal système. Cette option est prise en charge sur Windows 8 et Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_INDEPENDENT_SESSION_MODE</strong>(0x08000000)</td>
<td>Indique qu’une session de journalisation ne doit pas être affectée par les échecs de <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> dans d’autres sessions. Sans cet indicateur, si un événement ne peut pas être publié dans l’une des sessions pour lesquelles un fournisseur est activé, l’événement n’est pas publié dans les sessions. Lorsque cet indicateur est défini, l’échec de l’écriture d’un événement dans une session ne fait pas en sorte que la fonction <strong>EventWrite</strong> retourne un code d’erreur dans d’autres sessions. <br/> Ne pas utiliser avec <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>. <br/> Cette option est prise en charge sur Windows 8.1, Windows Server 2012 R2 et versions ultérieures.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING</strong> (0x10000000)</td>
<td>Écrit des événements qui ont été enregistrés sur des processeurs différents dans une mémoire tampon commune. L’utilisation de ce mode peut éliminer le problème des événements qui apparaissent dans le désordre lorsque des événements sont publiés sur des processeurs différents à l’aide de l’heure système. Ce mode peut également éliminer le problème avec les journaux circulaires qui s’affichent pour supprimer des événements sur plusieurs ordinateurs de processeur.<br/> Si vous n’utilisez pas ce mode et que vous utilisez l’heure système, les événements peuvent apparaître dans le désordre sur plusieurs ordinateurs de processeur. Cela est dû au fait que les mémoires tampons ETW sont associées à un processeur au lieu d’un thread. Par conséquent, si un thread passe d’un processeur à un autre, la mémoire tampon associée à ce dernier peut être vidée sur le disque avant celle associée à l’UC précédente.<br/> Si vous vous attendez à un volume élevé d’événements (par exemple, plus de 1 000 événements par seconde), vous ne devez pas utiliser ce mode.<br/> Notez que le numéro de processeur n’est pas inclus avec l’événement.<br/> Cette option est prise en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_ADDTO_TRIAGE_DUMP</strong>(0x80000000)</td>
<td>Cette option ajoute des mémoires tampons ETW aux vidages de triage. Cette option est prise en charge sur Windows 8 et Windows Server 2012. <br/></td>
</tr>
</tbody>
</table>
