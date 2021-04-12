---
title: Messages
description: Les rubriques de cette section fournissent les spécifications de référence pour les messages d’entrée de pointeur spécifiques et les notifications.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381937"
---
# <a name="messages"></a>Messages

Les rubriques de cette section fournissent les spécifications de référence pour les [messages d’entrée de pointeur spécifiques et les notifications](messages-and-notifications-portal.md).

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md)<br/></td>
<td>Envoyé à une fenêtre, lorsque l’entrée de pointeur est détectée pour la première fois, afin de déterminer la cible d’entrée la plus probable pour la [manipulation directe](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal). <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Publié lorsqu’un pointeur effectue un contact sur la zone non cliente d’une fenêtre. Le message cible la fenêtre sur laquelle le pointeur effectue un contact. Le pointeur est capturé implicitement dans la fenêtre afin que la fenêtre continue à recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact. <br/> Si une fenêtre a capturé ce pointeur, ce message n’est pas publié. Au lieu de cela, un [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) est publié dans la fenêtre qui a capturé ce pointeur. <br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Publié lorsqu’un pointeur qui a effectué le contact sur la zone non cliente d’une fenêtre interrompt le contact. Le message cible la fenêtre sur laquelle le pointeur crée un contact et le pointeur est, à ce stade, capturé implicitement dans la fenêtre afin que la fenêtre continue de recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact, y compris la notification [<strong>WM_NCPOINTERUP</strong>] (WM-ncpointerup.MD). <br/> Si une fenêtre a capturé ce pointeur, ce message n’est pas publié. Au lieu de cela, un [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) est publié dans la fenêtre qui a capturé ce pointeur. <br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Publié pour fournir une mise à jour sur un pointeur qui a effectué un contact sur la zone non cliente d’une fenêtre ou lorsqu’un contact de pointage non capturé se déplace au-dessus de la zone non cliente d’une fenêtre. Pendant que le pointeur pointe, le message cible la fenêtre sur laquelle le pointeur se trouve. Tandis que le pointeur est en contact avec la surface, le pointeur est capturé implicitement dans la fenêtre sur laquelle le pointeur a été contacté et cette fenêtre continue à recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact. <br/> Si une fenêtre a capturé ce pointeur, ce message n’est pas publié. Au lieu de cela, un [<strong>WM_POINTERUPDATE</strong>] (WM-pointerupdate.MD) est publié dans la fenêtre qui a capturé ce pointeur.<br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Envoyé à une fenêtre lorsqu’une action importante se produit dans une fenêtre descendante. Ce message est maintenant étendu pour inclure l’événement [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD). Lorsque la fenêtre enfant est créée, le système envoie [<strong>WM_PARENTNOTIFY</strong>] (/Previous-versions/Windows/Desktop/inputmsg/WM-parentnotify) juste avant la fonction [<strong>CreateWindow</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowa) ou [<strong>CreateWindowEx</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowexa) qui crée la fenêtre retourne. Lorsque la fenêtre enfant est détruite, le système envoie le message avant tout traitement pour détruire la fenêtre.<br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)). <br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Envoyé à une fenêtre inactive lorsqu’un pointeur principal génère une [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) sur la fenêtre. Tant que le message reste non géré, il se déplace vers le haut de la chaîne de la fenêtre parente jusqu’à ce qu’il atteigne la fenêtre de niveau supérieur. Les applications peuvent répondre à ce message pour spécifier s’ils souhaitent être activés.<br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)). <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Envoyé à une fenêtre qui perd la capture d’un pointeur d’entrée.<br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Envoyé à une fenêtre en cas de modification des paramètres d’une analyse à laquelle un digitaliseur est attaché. Ce message contient des informations relatives à la mise à l’échelle du mode d’affichage. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Envoyé à une fenêtre lorsqu’un dispositif de pointage est détecté dans la plage d’un numériseur d’entrée. Ce message contient des informations relatives à l’appareil et à sa proximité. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Envoyé à une fenêtre lorsqu’un appareil de pointeur a fait l’ensemble de la plage d’un numériseur d’entrée. Ce message contient des informations relatives à l’appareil et à sa proximité. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Publié lorsqu’un pointeur effectue un contact sur la zone cliente d’une fenêtre. Ce message d’entrée cible la fenêtre sur laquelle le pointeur effectue un contact, et le pointeur est capturé implicitement dans la fenêtre afin que la fenêtre continue de recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Envoyé à une fenêtre lorsqu’un nouveau pointeur entre dans la plage de détection sur la fenêtre (survol) ou lorsqu’un pointeur existant se déplace dans les limites de la fenêtre. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Envoyé à une fenêtre lorsqu’un pointeur quitte la plage de détection sur la fenêtre (pointage) ou lorsqu’un pointeur se déplace à l’extérieur des limites de la fenêtre. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Se produit sur le processus qui reçoit l’entrée lorsque l’entrée du pointeur est routée vers un autre processus.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Envoyé à tous les processus (configurés pour le chaînage inter-processus via [<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) et ne gérant pas actuellement l’entrée de pointeur) jamais associé à un ID de pointeur spécifique, lorsqu’un message [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) est reçu sur le processus en cours. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Envoyé lors de l’entrée de pointeur en cours, pour un ID de pointeur existant, passe d’un processus à un autre dans le contenu configuré pour le chaînage entre processus ([<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Publié lorsqu’un pointeur qui a effectué le contact sur la zone cliente d’une fenêtre interrompt le contact. Ce message d’entrée cible la fenêtre sur laquelle le pointeur crée un contact et le pointeur est, à ce stade, capturé implicitement dans la fenêtre afin que la fenêtre continue à recevoir des messages d’entrée, y compris la notification [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) pour le pointeur jusqu’à ce qu’il interrompe le contact. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)). <br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Publié pour fournir une mise à jour sur un pointeur qui a effectué un contact sur la zone cliente d’une fenêtre ou sur un pointeur non capturé pointant sur la zone cliente d’une fenêtre. Pendant que le pointeur pointe, le message cible la fenêtre sur laquelle le pointeur se trouve. Tandis que le pointeur est en contact avec la surface, le pointeur est capturé implicitement dans la fenêtre sur laquelle le pointeur a été contacté et cette fenêtre continue à recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact. <br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md)<br/></td>
<td>Publié dans la fenêtre avec le focus clavier de premier plan quand une roulette de défilement est pivotée. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md)<br/></td>
<td>Publié dans la fenêtre avec le focus clavier de premier plan quand une roulette de défilement horizontale est pivotée. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [<strong>WindowProc</strong>] (/Previous-versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md)<br/></td>
<td>Envoyé à une fenêtre d’une commande tactile pour déterminer la cible tactile la plus probable. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de message d’entrée de pointeur](wmpointer-reference.md)
</dt> </dl>

 

