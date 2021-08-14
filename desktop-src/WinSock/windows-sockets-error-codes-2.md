---
description: Windows Codes d’erreur de Sockets (Winsock) retournés par la fonction WSAGetLastError.
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: Windows Codes d’erreur des sockets (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece53093e7aca31d9d883680005f92ca8b30a76120209affb4dba42d6826d0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322002"
---
# <a name="windows-sockets-error-codes"></a>Windows Codes d’erreur des sockets

la plupart des Windows fonctions sockets 2 ne retournent pas la cause spécifique d’une erreur quand la fonction retourne. Pour plus d’informations, consultez la rubrique [gestion des erreurs Winsock](handling-winsock-errors.md) .

La fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne la dernière erreur qui s’est produite pour le thread appelant. quand une fonction Windows sockets particulière indique qu’une erreur s’est produite, cette fonction doit être appelée immédiatement pour récupérer le code d’erreur étendu pour l’appel de fonction ayant échoué. Ces codes d’erreur et une brève description de texte associée à un code d’erreur sont définis dans le fichier d’en-tête *winerror. h* . La fonction [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) peut être utilisée pour obtenir la chaîne de message de l’erreur retournée.

Pour plus d’informations sur la gestion des codes d’erreur lors du Portage d’applications de socket vers Winsock, consultez [codes d’erreur-errno, h \_ errno et WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md).

La liste suivante décrit les codes d’erreur possibles retournés par la fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Les erreurs sont répertoriées dans l’ordre numérique avec le nom de la macro d’erreur. Certains codes d’erreur définis dans le fichier d’en-tête *Winsock2. h* ne sont pas retournés par une fonction.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Code/valeur de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="WSA_INVALID_HANDLE"></span><span id="wsa_invalid_handle"></span><dl> <dt><strong>WSA_INVALID_HANDLE</strong></dt> <dt>6</dt> </dl></td>
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>Le descripteur d’objet d’événement spécifié n’est pas valide.</dt> <dd> Une application tente d’utiliser un objet d’événement, mais le handle spécifié n’est pas valide.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>Mémoire disponible insuffisante.</dt> <dd> une application a utilisé une fonction de sockets Windows qui correspond directement à une fonction Windows. la fonction Windows indique un manque de ressources mémoire requises.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>Un ou plusieurs paramètres ne sont pas valides.</dt> <dd> une application a utilisé une fonction de sockets Windows qui est directement mappée à une fonction Windows. la fonction Windows indique un problème avec un ou plusieurs paramètres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>Opération Overlapped abandonnée.</dt> <dd> Une opération avec chevauchement a été annulée en raison de la fermeture du socket ou de l’exécution de la commande SIO_FLUSH dans <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>Objet d’événement d’e/s avec chevauchement non signalé.</dt> <dd> L’application a essayé de déterminer l’état d’une opération avec chevauchement qui n’est pas encore terminée. Les applications qui utilisent <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>WSAGetOverlappedResult</strong></a> (avec l’indicateur <em>FWait</em> défini sur <strong>false</strong>) dans un mode d’interrogation pour déterminer à quel moment une opération Overlapped s’est terminée, récupérez ce code d’erreur jusqu’à ce que l’opération soit terminée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>Les opérations avec chevauchement seront terminées ultérieurement. <br/> <dl> <dt><span></span></dt> <dd> L'application a initialisé une opération avec chevauchement qui ne peut pas être achevée immédiatement. Une indication de saisie semi-automatique sera fournie ultérieurement une fois l’opération terminée.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>WSAEINTR</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>Appel de fonction interrompu.</dt> <dd> Une opération de blocage a été interrompue par un appel à <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>WSAEBADF</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>Le descripteur de fichier n’est pas valide.</dt> <dd> Le descripteur de fichier fourni n’est pas valide. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>WSAEACCES</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>Autorisation refusée.</dt> <dd> Une tentative a été effectuée pour accéder à un socket de manière interdite par ses autorisations d’accès. Par exemple, vous utilisez une adresse de diffusion pour <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> sans autorisation de diffusion définie à l’aide de <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a>(SO_BROADCAST). <br/> Une autre raison possible de l’erreur WSAEACCES est que lorsque la fonction <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>Bind</strong></a> est appelée (sur Windows NT 4,0 avec SP4 et versions ultérieures), un autre pilote d’application, de service ou de mode noyau est lié à la même adresse avec un accès exclusif. Ce type d’accès exclusif est une nouvelle fonctionnalité de Windows NT 4,0 avec SP4 et versions ultérieures, et est implémenté à l’aide de l’option <a href="/windows/desktop/winsock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>WSAEFAULT</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>Adresse incorrecte.</dt> <dd> Le système a détecté une adresse de pointeur non valide lors de la tentative d’utilisation d’un argument de pointeur d’un appel. Cette erreur se produit si une application passe une valeur de pointeur non valide, ou si la longueur de la mémoire tampon est trop petite. Par exemple, si la longueur d’un argument, qui est une structure <a href="/windows/desktop/winsock/sockaddr-2"><strong>sockaddr</strong></a> , est inférieure à sizeof (sockaddr).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>WSAEINVAL</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>Argument non valide.</dt> <dd> Un argument non valide a été fourni (par exemple, en spécifiant un niveau non valide pour la fonction <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> ). Dans certains cas, il fait également référence à l’état actuel du socket, par exemple en appelant <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>Accept</strong></a> sur un socket qui n’est pas à l’écoute.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>WSAEMFILE</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>Trop de fichiers ouverts.</dt> <dd> Trop de sockets ouverts. Chaque implémentation peut avoir un nombre maximal de descripteurs de Socket disponibles, globalement, par processus ou par thread.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>WSAEWOULDBLOCK</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>Ressource temporairement indisponible.</dt> <dd> Cette erreur est retournée à partir d’opérations sur des sockets non bloquants qui ne peuvent pas être terminés immédiatement, par exemple <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>recv</strong></a> quand aucune donnée n’est mise en file d’attente pour être lue à partir du Socket. Il s’agit d’une erreur récupérable et l’opération doit être retentée ultérieurement. Il est normal que WSAEWOULDBLOCK soit signalé comme résultat de l’appel de <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> sur un socket de SOCK_STREAM sans blocage, car un certain temps doit s’écouler avant que la connexion soit établie.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>WSAEINPROGRESS</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>Opération en cours.</dt> <dd> Une opération de blocage est actuellement en cours d'exécution. Windows Les sockets n’autorisent qu’une seule opération de blocage (par tâche ou par thread) en suspens, et si un autre appel de fonction est effectué (qu’il référence ou non ce Socket ou un autre), la fonction échoue avec l’erreur WSAEINPROGRESS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>WSAEALREADY</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>Opération déjà en cours.</dt> <dd> Une opération a été tentée sur un socket non bloquant avec une opération déjà en cours, c’est-à-dire appeler <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> une deuxième fois sur un socket non bloquant qui se connecte déjà, ou annuler une demande asynchrone (<strong>WSAAsyncGetXbyY</strong>) qui a déjà été annulée ou terminée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>WSAENOTSOCK</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Opération de socket sur un qui n’est pas Socket.</dt> <dd> Une opération a été tentée sur un qui n’est pas un Socket. Le paramètre de handle de socket ne faisait pas référence à un socket valide ou, pour <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>Select</strong></a>, un membre d’un <strong>FD_SET</strong> n’est pas valide.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>WSAEDESTADDRREQ</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>Adresse de destination requise.</dt> <dd> Une adresse requise a été omise d’une opération sur un Socket. Par exemple, cette erreur est retournée si <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> est appelé avec l’adresse distante de ADDR_ANY.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>WSAEMSGSIZE</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>Message trop long.</dt> <dd> Un message envoyé sur un socket datagramme était plus volumineux que le tampon de messages interne ou une autre limite réseau, ou le tampon utilisé pour recevoir un datagramme était plus petit que le datagramme lui-même.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>WSAEPROTOTYPE</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>Type de protocole incorrect pour le Socket.</dt> <dd> Un protocole a été spécifié dans l’appel de fonction <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socket</strong></a> qui ne prend pas en charge la sémantique du type de socket demandé. Par exemple, le protocole UDP ARPA Internet ne peut pas être spécifié avec un type de socket de SOCK_STREAM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>WSAENOPROTOOPT</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>Option de protocole incorrecte.</dt> <dd> Une option ou un niveau inconnu, non valide ou non pris en charge a été spécifié dans un appel <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>getsockopt</strong></a> ou <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>WSAEPROTONOSUPPORT</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>Protocole non pris en charge.</dt> <dd> Le protocole demandé n’a pas été configuré dans le système, ou aucune implémentation de ce dernier n’existe. Par exemple, un appel de <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socket</strong></a> demande un socket SOCK_DGRAM, mais spécifie un protocole de flux.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>WSAESOCKTNOSUPPORT</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>Type de socket non pris en charge.</dt> <dd> La prise en charge du type de socket spécifié n'existe pas dans cette famille d'adresses. Par exemple, le type facultatif SOCK_RAW peut être sélectionné dans un appel <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socket</strong></a> , et l’implémentation ne prend pas en charge SOCK_RAW Sockets.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>WSAEOPNOTSUPP</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>Opération non prise en charge.</dt> <dd> L’opération tentée n’est pas prise en charge pour le type d’objet référencé. Cela se produit généralement lorsqu’un descripteur de socket sur un socket qui ne peut pas prendre en charge cette opération tente d’accepter une connexion sur un socket datagramme.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>WSAEPFNOSUPPORT</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>Famille de protocoles non prise en charge.</dt> <dd> La famille de protocoles n’a pas été configurée dans le système ou aucune implémentation de celle-ci n’existe. Ce message a une signification légèrement différente de WSAEAFNOSUPPORT. toutefois, il est interchangeable dans la plupart des cas, et toutes les fonctions de sockets Windows qui retournent l’un de ces messages spécifient également WSAEAFNOSUPPORT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>WSAEAFNOSUPPORT</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>Famille d’adresses non prise en charge par la famille de protocoles.</dt> <dd> Une adresse incompatible avec le protocole demandé a été utilisée. Tous les sockets sont créés avec une famille d’adresses associée (autrement dit, AF_INET pour les protocoles Internet) et un type de protocole générique (c’est-à-dire, SOCK_STREAM). Cette erreur est retournée si un protocole incorrect est demandé explicitement dans l’appel de <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socket</strong></a> ou si une adresse de la famille incorrecte est utilisée pour un socket, par exemple, dans <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>WSAEADDRINUSE</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>Adresse déjà utilisée.</dt> <dd> En règle générale, une seule utilisation de chaque adresse de socket (protocole/adresse IP/port) est autorisée. Cette erreur se produit si une application tente de <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>lier</strong></a> un socket à une adresse IP/un port qui a déjà été utilisé pour un socket existant, ou un socket qui n’a pas été fermé correctement ou qui est encore en cours de fermeture. Pour les applications serveur qui doivent <strong>lier</strong> plusieurs sockets au même numéro de port, envisagez d’utiliser <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> (SO_REUSEADDR). Généralement, les applications clientes n’ont pas besoin d’appeler <strong>Bind</strong> ,<a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> choisit automatiquement un port inutilisé. Lorsque <strong>Bind</strong> est appelé avec une adresse générique (impliquant ADDR_ANY), une erreur WSAEADDRINUSE peut être retardée jusqu’à ce que l’adresse spécifique soit validée. Cela peut se produire avec un appel à une autre fonction plus tard, y compris <strong>Connect</strong>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>Listen</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>ou <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>WSAEADDRNOTAVAIL</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>Impossible d’assigner l’adresse demandée.</dt> <dd> L’adresse demandée n’est pas valide dans son contexte. Cela résulte généralement d’une tentative de <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>liaison</strong></a> à une adresse qui n’est pas valide pour l’ordinateur local. Cela peut également être dû à <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a>, <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>ou <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>WSASendTo</strong></a> lorsque l’adresse ou le port distant n’est pas valide pour un ordinateur distant (par exemple, une adresse ou un port 0).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>WSAENETDOWN</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>Le réseau est en défaillance.</dt> <dd> Une opération de socket a rencontré un réseau inactif. Cela pourrait indiquer un sérieux problème du système réseau (c'est-à-dire, la pile de protocoles sur lequel la DLL de sockets Windows s'exécute), de l'interface réseau ou du réseau local lui-même.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>WSAENETUNREACH</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>Le réseau est inaccessible.</dt> <dd> Une opération de socket a été tentée sur un réseau inaccessible. Cela signifie généralement que le logiciel local ne sait aucun itinéraire pour atteindre l’hôte distant.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>WSAENETRESET</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>La connexion réseau a été abandonnée lors de la réinitialisation.</dt> <dd> La connexion a été interrompue en raison d’une activité de maintien en état de la détection d’un échec pendant l’opération. Elle peut également être retournée par <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> si une tentative est faite pour définir <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> sur une connexion qui a déjà échoué.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>WSAECONNABORTED</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>Le logiciel a provoqué l’abandon de la connexion.</dt> <dd> Une connexion établie a été abandonnée par le logiciel sur votre ordinateur hôte, peut-être en raison d’un délai d’attente de transmission de données ou d’une erreur de protocole.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>WSAECONNRESET</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>Connexion réinitialisée par l’homologue.</dt> <dd> une connexion existante a dû être fermée par l’hôte distant. Cela se produit généralement si l’application homologue sur l’hôte distant est soudainement arrêtée, que l’hôte est redémarré, que l’hôte ou l’interface réseau distante est désactivé, ou que l’hôte distant utilise une fermeture matérielle (consultez <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> pour plus d’informations sur l’option SO_LINGER sur le socket distant). Cette erreur peut également se produire si une connexion a été interrompue en raison d’une activité de maintien en état de la détection d’un échec alors qu’une ou plusieurs opérations sont en cours. Les opérations qui étaient en cours échouent avec WSAENETRESET. Les opérations suivantes échouent avec WSAECONNRESET.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>WSAENOBUFS</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>Aucun espace de mémoire tampon n’est disponible.</dt> <dd> Impossible d’effectuer une opération sur un socket en raison de l’insuffisance de l’espace de mémoire tampon du système ou de la saturation de la file d’attente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>WSAEISCONN</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>Le socket est déjà connecté.</dt> <dd> Une demande de connexion a été effectuée sur un socket déjà connecté. Certaines implémentations retournent également cette erreur si <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> est appelé sur un socket SOCK_DGRAM connecté (pour les sockets SOCK_STREAM, le paramètre <em>to</em> dans <strong>sendto</strong> est ignoré), bien que d’autres implémentations considèrent cela comme une occurrence légale.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>WSAENOTCONN</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>Le socket n’est pas connecté.</dt> <dd> Une demande d’envoi ou de réception de données n’a pas été autorisée car le socket n’est pas connecté et (lors de l’envoi sur un socket datagramme avec <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>) aucune adresse n’a été fournie. Tout autre type d’opération peut également retourner cette erreur, par exemple, le paramètre <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> si la connexion a été réinitialisée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>WSAESHUTDOWN</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>Envoi impossible après l’arrêt du Socket.</dt> <dd> Une demande d’envoi ou de réception de données n’a pas été autorisée car le socket avait déjà été arrêté dans cette direction avec un appel d' <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>arrêt</strong></a> précédent. En appelant <strong>Shutdown</strong> , une fermeture partielle d’un socket est demandée, qui est un signal d’envoi ou de réception, ou les deux ont été interrompus.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>WSAETOOMANYREFS</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>Trop de références.</dt> <dd> Trop de références à un objet de noyau.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>WSAETIMEDOUT</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>Délai d’attente de la connexion dépassé.</dt> <dd> Une tentative de connexion a échoué car le tiers connecté n’a pas répondu correctement après une certaine période, ou la connexion établie a échoué car l’hôte connecté n’a pas répondu.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>WSAECONNREFUSED</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>Connexion refusée.</dt> <dd> Aucune connexion n’a pu être établie car l’ordinateur cible l’a refusé activement. Cela se produit généralement lorsque vous tentez de vous connecter à un service qui est inactif sur l’hôte étranger, c’est-à-dire un service sans application serveur en cours d’exécution.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>WSAELOOP</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>Impossible de traduire le nom.</dt> <dd> Impossible de convertir un nom.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>WSAENAMETOOLONG</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>Le nom est trop long.</dt> <dd> Un composant de nom ou un nom est trop long.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>WSAEHOSTDOWN</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>L’hôte est inactif.</dt> <dd> Une opération de socket a échoué car l’hôte de destination est en panne. Une opération de socket a rencontré un hôte mort. L’activité de mise en réseau sur l’hôte local n’a pas été lancée. Ces conditions sont plus susceptibles d’être indiquées par l’erreur WSAETIMEDOUT.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>WSAEHOSTUNREACH</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>Aucun itinéraire vers l’hôte.</dt> <dd> Une opération de socket a été tentée sur un hôte impossible à atteindre. Consultez WSAENETUNREACH.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>WSAENOTEMPTY</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>Le répertoire n’est pas vide.</dt> <dd> Impossible de supprimer un répertoire qui n’est pas vide.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>WSAEPROCLIM</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>Trop de processus.</dt> <dd> une implémentation de sockets Windows peut avoir une limite du nombre d’applications qui peuvent l’utiliser simultanément. <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> peut échouer avec cette erreur si la limite a été atteinte.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>WSAEUSERS</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>Quota utilisateur dépassé.</dt> <dd> Le quota de l’utilisateur est insuffisant. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>WSAEDQUOT</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>Quota de disque dépassé.</dt> <dd> Le quota de disque est insuffisant. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>WSAESTALE</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>Référence de handle de fichier périmée.</dt> <dd> La référence de descripteur de fichier n’est plus disponible. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>WSAEREMOTE</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>L’élément est distant.</dt> <dd> L’élément n’est pas disponible localement. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>WSASYSNOTREADY</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>Le sous-système réseau n’est pas disponible.</dt> <dd> cette erreur est retournée par <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> si l’implémentation de sockets Windows ne peut pas fonctionner pour l’instant, car le système sous-jacent utilisé pour fournir des services réseau n’est pas disponible actuellement. Les utilisateurs doivent vérifier :<br/> </dd> </dl>
<ul>
<li>que le fichier DLL de sockets Windows approprié se trouve dans le chemin d’accès actuel.</li>
<li>qu’ils n’essaient pas d’utiliser plusieurs Windows implémentations de sockets simultanément. S’il existe plusieurs DLL WinSock sur votre système, assurez-vous que la première dans le chemin d’accès est appropriée pour le sous-système réseau actuellement chargé.</li>
<li>la documentation sur l’implémentation d’Windows sockets pour vérifier que tous les composants nécessaires sont actuellement installés et configurés correctement.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>WSAVERNOTSUPPORTED</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span>Winsock.dll version hors limites.</dt> <dd> l’implémentation actuelle de sockets Windows ne prend pas en charge la version de spécification Windows sockets demandée par l’application. Vérifiez que l'accès ne porte pas sur d'anciens fichiers DLL de Windows Sockets.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>WSANOTINITIALISED</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>WSAStartup réussi n’a pas encore été effectué.</dt> <dd> Soit l’application n’a pas appelé <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> ni <strong>WSAStartup</strong> . L’application peut accéder à un socket que la tâche active en cours ne possède pas (c’est-à-dire, essayer de partager un socket entre des tâches) ou <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>WSACleanup</strong></a> a été appelé trop souvent.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>WSAEDISCON</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>Arrêt approprié en cours.</dt> <dd> Retourné par <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>WSARecv</strong></a> et <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>WSARecvFrom</strong></a> pour indiquer que le tiers distant a initié une séquence d’arrêt appropriée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>WSAENOMORE</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Plus de résultats.</dt> <dd> Aucun autre résultat ne peut être retourné par la fonction <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>WSAECANCELLED</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>L’appel a été annulé.</dt> <dd> Un appel à la fonction <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> a été effectué alors que cet appel était toujours en cours de traitement. L’appel a été annulé.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>WSAEINVALIDPROCTABLE</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>La table des appels de procédure n’est pas valide.</dt> <dd> La table des appels de procédure du fournisseur de services n’est pas valide. Un fournisseur de services a retourné une table de procédures erronée pour Ws2_32.dll. Cela est généralement dû à la <strong>valeur null</strong>d’un ou plusieurs des pointeurs de fonction.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>WSAEINVALIDPROVIDER</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>Le fournisseur de services n’est pas valide.</dt> <dd> Le fournisseur de services demandé n’est pas valide. Cette erreur est retournée par les fonctions <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>WSCGetProviderInfo</strong></a> et <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> si l’entrée de protocole spécifiée est introuvable. Cette erreur est également retournée si le fournisseur de services a retourné un numéro de version autre que 2,0.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>WSAEPROVIDERFAILEDINIT</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>Échec de l’initialisation du fournisseur de services.</dt> <dd> Impossible de charger ou d’initialiser le fournisseur de services demandé. Cette erreur est retournée si la DLL du fournisseur de services n’a pas pu être chargée (échec de<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> ) ou si la fonction <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>WSPStartup</strong></a> ou <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>NSPStartup</strong></a> du fournisseur a échoué.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>WSASYSCALLFAILURE</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>Échec de l’appel système.</dt> <dd> Un appel système qui ne doit jamais échouer a échoué. Il s’agit d’un code d’erreur générique, renvoyé sous différentes conditions. <br/> Retourné lorsqu’un appel système qui ne doit jamais échouer échoue. Par exemple, si un appel à <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>WaitForMultipleEvents</strong></a> échoue ou si l’une des fonctions de registre ne parvient pas à manipuler les catalogues de protocole/d’espace de noms.<br/> Retourné lorsqu’un fournisseur ne retourne pas de réussite et ne fournit pas de code d’erreur étendu. Peut indiquer une erreur d’implémentation du fournisseur de services.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>Service introuvable.</dt> <dd> Aucun service de ce type n’est connu. Le service est introuvable dans l’espace de noms spécifié.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>Type de classe introuvable.</dt> <dd> La classe spécifiée est introuvable.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Plus de résultats.</dt> <dd> Aucun autre résultat ne peut être retourné par la fonction <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>L’appel a été annulé.</dt> <dd> Un appel à la fonction <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> a été effectué alors que cet appel était toujours en cours de traitement. L’appel a été annulé.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>WSAEREFUSED</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>La requête de base de données a été refusée.</dt> <dd> Une requête de base de données a échoué car elle a été refusée activement.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>Hôte introuvable.</dt> <dd> Hôte inconnu. Le nom n’est pas un nom d’hôte ou un alias officiel, ou il est introuvable dans la ou les bases de données interrogées. Cette erreur peut également être renvoyée pour les requêtes de protocole et de service, et signifie que le nom spécifié est introuvable dans la base de données appropriée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>Hôte ne faisant pas autorité introuvable.</dt> <dd> Il s’agit généralement d’une erreur temporaire lors de la résolution du nom d’hôte et signifie que le serveur local n’a pas reçu de réponse d’un serveur faisant autorité. Il est parfois possible de résoudre le problème en réessayant ultérieurement.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>Il s’agit d’une erreur irrécupérable.</dt> <dd> Cela indique qu’une erreur non récupérable s’est produite lors de la recherche d’une base de données. Cela peut être dû au fait que les fichiers de base de données (par exemple, les hôtes compatibles BSD, les SERVICES ou les fichiers de protocoles) sont introuvables ou qu’une requête DNS a été renvoyée par le serveur avec une erreur grave.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>Nom valide, aucun enregistrement de données du type demandé.</dt> <dd> Le nom demandé est valide et a été trouvé dans la base de données, mais il n’a pas les données associées appropriées en cours de résolution pour. L’exemple habituel est la tentative de conversion d’un nom d’hôte en adresse (à l’aide de <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> ou <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>WSAAsyncGetHostByName</strong></a>) qui utilise le DNS (Domain Name Server). Un enregistrement MX est retourné, mais aucun enregistrement A, indiquant que l’hôte lui-même existe, mais qu’il n’est pas directement accessible.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>Récepteurs QoS.</dt> <dd> Au moins une réserve de QoS est arrivée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>Expéditeurs QoS.</dt> <dd> Au moins un chemin d’envoi QoS est arrivé.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>Aucun expéditeur QoS.</dt> <dd> Il n’existe aucun expéditeur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>Aucun destinataire QoS.</dt> <dd> Il n’existe aucun destinataire QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>Demande QoS confirmée.</dt> <dd> La demande de réserve de QoS a été confirmée.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>Erreur d’admission QoS.</dt> <dd> Une erreur de QoS s’est produite en raison d’un manque de ressources.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>Échec de la stratégie QoS.</dt> <dd> La demande QoS a été rejetée, car le système de stratégie n’a pas pu allouer la ressource demandée au sein de la stratégie existante. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>Style QoS incorrect.</dt> <dd> Un style QoS inconnu ou en conflit a été rencontré.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>Objet de mauvaise qualité QoS.</dt> <dd> Un problème a été rencontré avec une partie du filterspec ou de la mémoire tampon spécifique au fournisseur en général.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>Erreur de contrôle du trafic QoS.</dt> <dd> Une erreur avec l’API de contrôle du trafic (TC) sous-jacente comme requête de QoS générique a été convertie pour la contrainte locale par l’API TC. Cela peut être dû à une erreur de mémoire insuffisante ou à une erreur interne du fournisseur QoS. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>Erreur générique QoS.</dt> <dd> Erreur de QoS générale.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>Erreur de type de service QoS.</dt> <dd> Un type de service non valide ou non reconnu a été trouvé dans le flowspec QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>Erreur QoS flowspec.</dt> <dd> Un flowspec non valide ou incohérent a été trouvé dans la structure <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>QoS</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>Mémoire tampon du fournisseur QoS non valide.</dt> <dd> Mémoire tampon spécifique au fournisseur QoS non valide.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>Style de filtre QoS non valide.</dt> <dd> Un style de filtre QoS non valide a été utilisé.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>Type de filtre QoS non valide.</dt> <dd> Un type de filtre QoS non valide a été utilisé.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>Nombre de filtres QoS incorrect.</dt> <dd> Un nombre incorrect de FILTERSPECs QoS a été spécifié dans le FLOWDESCRIPTOR.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>Longueur de l’objet QoS non valide.</dt> <dd> Un objet avec un champ ObjectLength non valide a été spécifié dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>Nombre de workflows QoS incorrect.</dt> <dd> Un nombre incorrect de descripteurs de workflow a été spécifié dans la structure QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>Objet QoS non reconnu.</dt> <dd> Un objet non reconnu a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>Objet de stratégie de qualité de service non valide.</dt> <dd> Un objet de stratégie non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>Descripteur de workflow QoS non valide.</dt> <dd> Un descripteur de workflow QoS non valide a été trouvé dans la liste des descripteurs de Flow.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>Flowspec spécifique au fournisseur QoS non valide.</dt> <dd> Un flowspec non valide ou incohérent a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>FILTERSPEC spécifique au fournisseur QoS non valide.</dt> <dd> Un FILTERSPEC non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>Objet en mode de rejet de forme QoS non valide.</dt> <dd> Un objet de mode de suppression de forme non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>Objet de taux de mise en forme QoS non valide.</dt> <dd> Un objet de taux de mise en forme non valide a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>Type d’élément QoS de la stratégie réservée.</dt> <dd> Un élément de stratégie réservée a été trouvé dans la mémoire tampon spécifique au fournisseur QoS.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winsock2. h ; </dt> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur-errno, h \_ errno et WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Gestion des erreurs Winsock](handling-winsock-errors.md)
</dt> <dt>

[**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
