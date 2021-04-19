---
title: Forum aux questions sur la méthode EAP
description: Fournit des réponses aux questions de programmation fréquemment posées sur la création de méthodes EAP.
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106509477"
---
# <a name="eap-method-frequently-asked-questions"></a>Forum aux questions sur la méthode EAP

Cette rubrique fournit des réponses aux questions de programmation fréquemment posées sur la création de méthodes EAP.

## <a name="eap-method-frequently-asked-questions"></a>Forum aux questions sur la méthode EAP



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
<td>Qu’est-ce que les &quot; données de configuration &quot; ?</td>
<td>Les termes &quot; données &quot; de configuration et &quot; données de connexion &quot; sont synonymes.</td>
</tr>
<tr class="even">
<td>Qu’est-ce que les &quot; données de connexion &quot; ?</td>
<td>&quot;Les données &quot; de connexion sont un objet blob opaque spécifique à une méthode EAP qui contient des informations de configuration pour la méthode. Ces données de connexion sont créées par la méthode lorsqu’elle est initialement configurée et ne sont jamais interprétées ou modifiées par un autre composant que la méthode EAP elle-même.</td>
</tr>
<tr class="odd">
<td>Que sont les &quot; informations d’identification &quot; ?</td>
<td>Les termes &quot; informations d’identification &quot; et &quot; données utilisateur &quot; sont synonymes.</td>
</tr>
<tr class="even">
<td>Qu’est-ce que les &quot; données utilisateur &quot; ?</td>
<td>&quot;Les données utilisateur &quot; sont un objet blob opaque spécifique à une méthode EAP qui contient des données d’identification utilisateur, telles qu’un nom d’utilisateur et un mot de passe. Les données utilisateur ne sont jamais interprétées ou modifiées par un autre composant que la méthode EAP elle-même. Les termes &quot; données &quot; et &quot; informations d’identification de l’utilisateur &quot; sont synonymes.</td>
</tr>
<tr class="odd">
<td>Qu’est-ce qu’un &quot; attribut EAP &quot; ?</td>
<td>Un &quot; attribut EAP &quot; est une structure de données qui contient un type de données prédéterminé. Les attributs sont utilisés pour communiquer des informations entre les méthodes EAP et les demandeurs, ou entre les méthodes EAP et les authentificateurs. Les implémentations d’homologue et d’authentificateur d’une méthode EAP peuvent échanger ces attributs sur un réseau.</td>
</tr>
<tr class="even">
<td>L’API de configuration et l’API Runtime peuvent-elles apparaître dans la même DLL de méthode ?</td>
<td>Oui. Veillez à spécifier la distinction lors de la configuration des entrées de Registre pour la méthode EAP elle-même. Le chemin d’accès de configuration et le chemin d’accès de l’homologue doivent être identiques.</td>
</tr>
<tr class="odd">
<td>L’API de configuration et l’API Runtime peuvent-elles apparaître dans des dll de méthode distinctes ?</td>
<td>Oui. Veillez à spécifier la distinction lors de la configuration des entrées de Registre pour la méthode EAP elle-même. Les chemins d’accès de configuration et d’homologue doivent pointer vers les dll correctes.</td>
</tr>
<tr class="even">
<td>Comment faire installer une méthode EAP ?</td>
<td>Pour installer une méthode EAP, vous devez d’abord implémenter [<strong>DllRegisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DllRegisterServer) et [<strong>DllUnregisterServer</strong>] (/Windows/Win32/API/OLECTL/NF-OLECTL-DLLUNREGISTERSERVER) dans la dll de méthode EAP elle-même. Ensuite, utilisez <strong>regsvr32.exe</strong> pour installer et désinstaller la méthode. Les clés de Registre appropriées doivent également être définies. Pour plus d’informations, consultez [installation d’une méthode EAP](installing-an-eap-method.md).<br/></td>
</tr>
<tr class="odd">
<td>Qu’est-ce que la prise en charge de la [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP) intrabande ?</td>
<td>Lorsque la prise en charge de la protection d’accès réseau intrabande est activée, les paquets NAP sont transportés dans les paquets de méthode EAP. En revanche, lorsque la prise en charge de la protection d’accès réseau hors bande est activée, l’échange [de déclaration d’intégrité](https://go.microsoft.com/fwlink/p/?linkid=83917) NAP se produit par le biais d’autres types de paquets de méthodes internes aux protocoles EAP, et les certificats générés par la protection d’accès réseau sont utilisés dans l’authentification de la méthode EAP.</td>
</tr>
<tr class="even">
<td>Puis-je activer la prise en charge NAP intrabande pour ma méthode EAP ?</td>
<td>Oui, la prise en charge de la protection d’accès réseau intrabande pour votre méthode EAP peut être activée. Pour plus d’informations, consultez [activation de la prise en charge de In-Band NAP pour les méthodes EAP](enabling-in-band-nap-support.md).</td>
</tr>
<tr class="odd">
<td>Comment fonctionne l’authentification flexible EAP via le tunneling sécurisé (EAP-FAST) ?</td>
<td>Le scénario EAP-FAST fonctionne comme suit. <br/>
<ul>
<li>La méthode traite une modification de mot de passe au niveau de l’authentification unique (SSO) utilisant l’interface utilisateur de la méthode.</li>
<li>La méthode retourne l’attribut [<strong>eatCredentialsChanged</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type).</li>
<li>Le demandeur indique à l’utilisateur que les informations d’identification ont changé et demande à l’utilisateur de saisir à nouveau ses informations d’identification.</li>
<li>Le demandeur saisit à nouveau les informations d’identification de l’utilisateur et les envoie à la méthode.</li>
</ul>
Pour plus d’informations sur EAP-FAST, consultez [authentification flexible EAP via](https://go.microsoft.com/fwlink/p/?linkid=84010) EAP-FAST.</td>
</tr>
<tr class="even">
<td>Qu’est-ce qu’une clé prépartagée (PSK) ?</td>
<td>Méthode permettant de transmettre et de recevoir des signaux numériques dans lesquels la phase d’un signal transmis est modifiée pour transmettre des informations. Le champ d’entrée [<strong>EAPConfigInputPSK</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_config_input_field_type) contient l’EAP-FAST PSK de l’utilisateur.</td>
</tr>
<tr class="odd">
<td>Qu’est-ce que WOW et quel est l’impact sur EAPHost ?</td>
<td>Microsoft Windows-32-bit-on-Windows-64-bit (WOW) est un composant du système d’exploitation dans Windows 64 bits qui prend en charge l’application de plateforme x86 32 bits. En règle générale, un auteur de méthode EAP définit une forme de structure C/C++ pour encapsuler les données de configuration, les données d’identification et les données d’interface utilisateur interactives. Pour éviter les incompatibilités dans WOW et dans d’autres scénarios, il est important de s’assurer que les structures de données sont alignées de façon similaire dans différentes architectures de processeur (processeurs 32 bits et 64 bits). En général, le remplissage factice est utilisé pour aligner les champs afin que la configuration, les informations d’identification et les données d’interface utilisateur interactives soient identiques sur les processeurs 32 et 64 bits.</td>
</tr>
<tr class="even">
<td>Quels sont les &quot; codes d’action &quot; et dans quelles conditions ces codes d’action sont-ils renvoyés ?</td>
<td>&quot;Les codes d’action &quot; permettent aux méthodes de contrôler le déroulement de l’authentification et font partie intégrante de l’ordinateur d’État. Il s’agit de valeurs retournées par une méthode EAP pour indiquer la prochaine action que EAPHost doit prendre. Par exemple, un code d’action peut indiquer à EAPHost que la méthode EAP a un paquet prêt pour la transmission. Le demandeur respecte tous les codes d’action retournés par une méthode EAP, mais ne publie jamais de codes d’action. Pour plus d’informations, consultez [codes d’action du demandeur d’homologue EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).<br/></td>
</tr>
<tr class="odd">
<td>Quand une méthode retourne [<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) et qu’est-ce que ce code d’action signifie pour EAPHost ?</td>
<td>[<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) est retourné par une méthode EAP pour indiquer à EAPHost qu’il doit ignorer le paquet qu’il a fourni à la méthode. Plus précisément, la méthode a déterminé que le paquet n’est pas valide. EAPHost attend ensuite le package suivant.</td>
</tr>
<tr class="even">
<td>Quand une méthode retourne [<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) et qu’est-ce que ce code d’action signifie pour EAPHost ?</td>
<td>[<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) est retourné par une méthode EAP pour indiquer à EAPHost que le paquet suivant reçu par EAPHost doit être envoyé au serveur d’accès réseau (NAS).</td>
</tr>
<tr class="odd">
<td>Quand une méthode retourne [<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) et qu’est-ce que ce code d’action signifie pour EAPHost ?</td>
<td>[<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) est retourné par une méthode EAP pour indiquer à EAPHost que la session d’authentification est terminée et que les résultats de cette session sont disponibles.</td>
</tr>
<tr class="even">
<td>Quand une méthode retourne [<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) et qu’est-ce que ce code d’action signifie pour EAPHost ?</td>
<td>[<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) est retourné par une méthode EAP pour indiquer à EAPHost que l’entrée utilisateur est requise pour poursuivre l’authentification, et qu’une boîte de dialogue d’interface utilisateur doit être affichée pour obtenir cette entrée. Une fois les données d’entrée utilisateur obtenues, EAPHost peut appeler à nouveau la méthode EAP avec les données de contexte d’interface utilisateur mises à jour.</td>
</tr>
<tr class="odd">
<td>Quand une méthode retourne [<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) et qu’est-ce que ce code d’action signifie pour EAPHost ?</td>
<td>[<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) est retourné par une méthode EAP pour indiquer à EAPHost que la méthode EAP a des attributs disponibles pour EAPHost à utiliser pendant l’authentification. EAPHost obtient les attributs en appelant la méthode [<strong>EapPeerGetResponseAttributes</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeergetresponseattributes) suivie d’un appel à la méthode [<strong>EapPeerSetResponseAttributes</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetresponseattributes).</td>
</tr>
<tr class="even">
<td>Quand une méthode retourne [<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) et qu’est-ce que ce code d’action signifie pour EAPHost ?</td>
<td>[<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) est retourné par une méthode EAP pour indiquer à EAPHost qu’aucune action n’est requise pour l’instant.</td>
</tr>
<tr class="odd">
<td>Puis-je activer le suivi du côté de l’authentificateur ?</td>
<td>Oui. Pour plus d’informations, consultez [activation du suivi](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur l’API de méthode homologue EAPHost](eap-host-peer-method-api-reference.md)
</dt> <dt>

[FAQ générale EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[FAQ du demandeur EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[FAQ sur le développement EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

