---
title: Forum aux questions sur le demandeur EAPHost
description: Cette rubrique fournit des réponses aux questions fréquemment posées sur l’API du demandeur EAPHost.
ms.assetid: bf8db711-386e-47c2-be47-4cfd6c4d8d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38e75220b186ef58f2b9f264f8f5fc0550a4119
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103735300"
---
# <a name="eaphost-supplicant-frequently-asked-questions"></a>Forum aux questions sur le demandeur EAPHost

Cette rubrique fournit des réponses aux questions fréquemment posées sur l’API du demandeur EAPHost.

### <a name="eaphost-supplicant-frequently-asked-questions"></a>Forum aux questions sur le demandeur EAPHost



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Question</th>
<th>Réponse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pourquoi dois-je appeler [<strong>EapHostPeerInitialize</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) et [<strong>EapHostPeerUninitialize</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) ?</td>
<td>[<strong>EapHostPeerInitialize</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) et [<strong>EapHostPeerUninitialize</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) initialisent et désinitialisent l’environnement com utilisé pour la communication interprocessus (IPC) entre un demandeur et EAPHost.</td>
</tr>
<tr class="even">
<td>Quelles fonctions doivent être appelées sur des threads qui ont initialisé COM pour [une thread cloisonné (STA, Single-Threaded Apartment](/previous-versions/ms810413(v=msdn.10)) ) ?</td>
<td>[<strong>EapHostPeerInvokeConfigUI</strong>] (/Previous-versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) et [<strong>EapHostAuthenticatorInvokeConfigUI</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodauthenticatorapis/NF-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui) doit être appelé sur les threads qui ont initialisé com pour STA. Pour ce faire, vous pouvez appeler l’API COM [<strong>CoInitialize</strong>] (/Windows/Win32/API/objbase/NF-objbase-CoInitialize); une fois le demandeur terminé, le thread STA [<strong>CoUninitialize</strong>] (/Windows/Win32/API/combaseapi/NF-combaseapi-CoUninitialize) doit être appelé avant de quitter.</td>
</tr>
<tr class="odd">
<td>Comment EAPHost exporte-t-il le matériel de génération ?</td>
<td>Les méthodes EAP EAPHost exportent les clés de session principale (MSKs) sous la forme de clés de chiffrement de point-à-point (MPPE) Microsoft pour les demandeurs. Des éléments de clé supplémentaires, tels que les clés principales par paire (PMKs), peuvent être générés par le demandeur à l’aide de MSK. Pour que les méthodes génèrent d’autres clés pendant l’authentification, les méthodes peuvent fournir ces clés en tant qu’attributs spécifiques au fournisseur pour les demandeurs.</td>
</tr>
<tr class="even">
<td>Qu’est-ce qu’une clé de session principale étendue (EMSK) ?</td>
<td>EMSK est un élément de génération de clé supplémentaire exporté par la méthode EAP. EMSK a une longueur d’au moins 64 octets. EMSK est partagé entre le client et le serveur EAP, mais n’est pas partagé avec l’authentificateur ou tout autre tiers. Actuellement, EMSK est réservé pour une utilisation ultérieure. Pour plus d’informations, consultez [EAP (Extensible Authentication Protocol) Configuration requise pour les réseaux locaux sans fil](https://go.microsoft.com/fwlink/p/?linkid=84064).<br/></td>
</tr>
<tr class="odd">
<td>Quand une méthode consomme ou génère-t-elle un attribut ?</td>
<td>Si une méthode EAP génère des attributs ou des EMSK, le demandeur utilisera des attributs. En règle générale, les attributs qui sont consommés par les demandeurs sont des clés. Les attributs utilisés sont <strong>eatPeerId</strong>, <strong>eatServerId</strong>, <strong>eatMethodId</strong>, <strong>eatEMSK</strong>et <strong>eatCredentialsChanged</strong>. Pour plus d’informations, consultez [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type). Une méthode EAP peut exporter des éléments EMSK supplémentaires spécifiques à l’application, tels que :
<ul>
<li>ID de la session</li>
<li>[Protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Quels attributs [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) consomme-t-il ?</td>
<td>Le demandeur [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) sans fil natif utilisera les attributs d’authentification EAPHost suivants :
<ul>
<li>Modifier la notification de mot de passe</li>
<li>Clés d’envoi/réception MPPE (Microsoft Point-to-Point Encryption). ID de la/de la = 331/16 et 311/1</li>
</ul>
Les clés MPPE sont des clés générées à la fin de la réussite de l’authentification, par l’homologue et l’authentificateur. Ces clés sont utilisées par [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) et le serveur d’accès réseau (NAS) pour chiffrer et déchiffrer les paquets envoyés et reçus.<br/></td>
</tr>
<tr class="odd">
<td>Quel est l’objectif de l’indicateur EAP_PEER_FLAG_GUEST_ACCESS dans EAPHost ?</td>
<td>Lorsque cet indicateur est défini dans [<strong>EAPHostPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession), EAPHost interprète cela comme une demande d’autorisation d’invité et retourne une réponse d’identité <strong>null</strong> qui est ensuite transmise au demandeur et renvoyée au serveur EAP.</td>
</tr>
<tr class="even">
<td>Comment le demandeur demande-t-il l’authentification de l’ordinateur ?</td>
<td>L’authentification de l’ordinateur est requise en définissant l’indicateur [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="odd">
<td>Comment le demandeur demande-t-il l’authentification de l’utilisateur ?</td>
<td>L’authentification utilisateur est demandée en ne définissant pas l’indicateur [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="even">
<td>Quand dois-je utiliser [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) au lieu de la fonction [<strong>EapHostFreeEapError</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror) ?</td>
<td>La fonction [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) est utilisée uniquement pour libérer des structures [<strong>EAP_ERROR</strong>] (/Windows/Desktop/API/eaptypes/NS-eaptypes-eap_error) retournées par les API de configuration EAPHost. Les API de configuration EAPHost sont définies dans EapHostPeerConfigApis. h. En revanche, la fonction [<strong>EapHostPeerFreeEapError</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror) est utilisée pour libérer <strong>EAP_ERROR</strong> structures retournées par les API d’exécution EAPHost. Les API d’exécution EAPHost sont définies dans EapPApis. h. N’utilisez jamais la version Runtime de l’API avec la version de configuration des API. pour ce faire, il peut produire des résultats inattendus.<br/></td>
</tr>
<tr class="odd">
<td>J’ai implémenté mon interface utilisateur dans le même thread que celui utilisé pour traiter une session d’authentification EAP sur le demandeur. Une fois que j’ai déclenché une boîte de dialogue d’interface utilisateur interactive pour obtenir des informations d’identification ou d’autres données d’entrée d’utilisateur, le prochain appel par EAPHost à une méthode d’homologue EAP échoue avec <strong>ERROR_OBJECT_DISCONNECTED</strong>. Pourquoi cela s’est-il produit et comment puis-je y remédier ?</td>
<td>Alors que les API EAPHost côté client sont toutes des API de style C, ces API C sont simplement des wrappers des API COM correspondantes. Les API de style C s’exécutent dans un environnement COM multithread. Le code d’interface utilisateur s’exécute généralement dans le modèle de thread cloisonné. Étant donné que les deux modèles de thread sont en conflit les uns avec les autres, n’exécutez pas le code d’interface utilisateur dans le thread qui traite les authentifications EAP.</td>
</tr>
<tr class="even">
<td>Pourquoi l’API [<strong>EapHostPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) prend-elle un pointeur de fonction de rappel [<em>NotificationHandler</em>] (/Previous-versions/Windows/Desktop/API) comme paramètre ?</td>
<td>[<em>NotificationHandler</em>] (/Previous-versions/Windows/Desktop/API) est le mécanisme par lequel un demandeur est informé qu’il doit s’authentifier de nouveau. Il existe plusieurs scénarios dans lesquels le demandeur est obligé de s’authentifier de nouveau, y compris l’authentification avec la [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</td>
</tr>
<tr class="odd">
<td>Quel est l’objectif du paramètre <em>pConnectionId</em> dans l’API [<strong>EapHostPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) ?</td>
<td><em>pConnectionId</em> est un pointeur vers une valeur Guid définie par le demandeur, utilisée pour identifier une connexion réseau qui appartient au demandeur. Lorsque la fonction de rappel [<em>NotificationHandler</em>] (/Previous-versions/Windows/Desktop/API) est appelée, ce GUID est transmis pour identifier la connexion réseau que le demandeur utilisera pour les demandes de réauthentification.</td>
</tr>
<tr class="even">
<td>Comment faire savoir s’il y a une modification de l’état de mise en quarantaine ?</td>
<td>L’utilisateur reçoit une notification visuelle d’une modification de l’état de mise en quarantaine uniquement s’il existe au moins une interface inscrite du client de mise en quarantaine de la protection d’accès réseau (NAP) (QEC) dans le système. Si c’est le cas, lorsque la nouvelle authentification est tentée, l’utilisateur est averti de la modification de l’état de mise en quarantaine via une fenêtre contextuelle.</td>
</tr>
<tr class="odd">
<td>Comment faire savoir s’il existe une interface QEC inscrite NAP dans le système ?</td>
<td>Ouvrez une fenêtre avec élévation de privilèges, puis exécutez la commande netsh suivante : &quot; netsh nap client Show State &quot; . Pour plus d’informations, consultez [commandes netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Si le demandeur s’authentifie de nouveau, quel ID de connexion le QEC doit-il utiliser lors de la réauthentification ?</td>
<td>Le QEC doit utiliser le même ID de connexion que celui utilisé pour la session précédente.</td>
</tr>
<tr class="odd">
<td>Il n’existe qu’une seule méthode du demandeur EAPHost disponible pour afficher les boîtes de dialogue de l’interface utilisateur, mais les méthodes EAP ont plusieurs types d’appels spécifiques à l’interface utilisateur. Quelle méthode le demandeur doit-il appeler lorsqu’il obtient le code d’action <strong>EapHostPeerResponseInvokeUI</strong> , indiquant que le demandeur doit afficher une boîte de dialogue d’interface utilisateur ?</td>
<td>Aucune action n’est requise par l’utilisateur, car EAPHost sait quelle fonction de méthode appeler. Par exemple, lorsque le code d’action <strong>EapHostPeerResponseInvokeUI</strong> est retourné, le demandeur appelle ces trois fonctions dans l’ordre suivant : [<strong>EapHostPeerGetUIContext</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeergetuicontext), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) et [<strong>EapHostPeerSetUIContext</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeersetuicontext).</td>
</tr>
<tr class="even">
<td>Quelle est la différence entre un objet BLOB d’informations d’identification et un objet BLOB de configuration ?</td>
<td>L’objet BLOB d’informations d’identification contient uniquement des données utilisateur telles que le nom d’utilisateur, le mot de passe et le code confidentiel. L’objet BLOB de configuration contient les paramètres qui contrôlent le comportement de la méthode.</td>
</tr>
<tr class="odd">
<td>Puis-je activer le suivi du côté client EAPHost ?</td>
<td>Oui. Pour plus d’informations, consultez [activation du suivi](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur l’API Supplier EAPHost](eap-host-supplicant-api-reference.md)
</dt> <dt>

[FAQ générale EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[FAQ sur les méthodes EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[FAQ sur le développement EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

