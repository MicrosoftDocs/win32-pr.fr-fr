---
title: Problèmes d’installation et de chargement de page
description: Problèmes d’installation et de chargement de page
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77fb7a41578463364837281dffcdfb22177e9785673049a65f05e9d0e33240e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358859"
---
# <a name="installation-and-page-loading-problems"></a>Problèmes d’installation et de chargement de page

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Lorsque je tente d’installer Microsoft Agent sur Microsoft Windows NT, j’obtiens un message indiquant que je dois être un administrateur.

Étant donné que Microsoft Agent écrit des fichiers dans votre répertoire système lors de l’installation de, vous devez disposer des privilèges administrateur (non utilisateur) pour installer.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Lorsque je tente d’installer Microsoft Agent, j’obtiens l’une des erreurs suivantes : Process (regsvr32/s Windows \\ msagent \\AgentCtl.dll). Erreur lors de la création de ce fichier. Impossible de trouver ce fichier. (Remarque : l’emplacement du répertoire mentionné dans le message d’erreur varie selon la façon dont vous avez installé Windows.) Un MSVCRT.DLL de DLL requis est introuvable. Erreur lors de la création du processus <c : \\ Windows \\ msagent \\agentsvr.exe/regserver>. Raison : l’un des fichiers de bibliothèque requis pour exécuter cette application est introuvable. (Remarque : l’emplacement du répertoire mentionné dans le message d’erreur varie selon la façon dont vous avez installé Windows.)

L’installation de Microsoft agent requiert l’installation correcte de Regsvr32.exe, Msvcrt.dll (la bibliothèque Runtime C de Microsoft) et des dll OLE à jour. Consultez Mise à jour DCOM : ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). Pour vous assurer que tous les fichiers système corrects sont présents, la meilleure méthode consiste à installer [Microsoft Internet Explorer 4,0](https://www.microsoft.com/ie/download) ou une version ultérieure.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Lorsque je tente de charger une page scriptée pour Microsoft Agent, j’obtiens une erreur de script : « VBScript Runtime Error, Object required ».

L’une des conditions suivantes peut entraîner l’affichage du message :

-   vos options de sécurité pour Microsoft Internet Explorer doivent être définies pour activer les contrôles de ActiveX et les plug-ins. Consultez la page sécurité de votre navigateur. dans Microsoft Internet Explorer, ouvrez le menu affichage, choisissez Options, cliquez sur l’onglet sécurité et assurez-vous que la case à cocher activer ActiveX les contrôles et les Plug-Ins est activée.
-   vous exécutez sur un système à double démarrage Windows 9x ou Windows NT et vous avez installé Microsoft Agent sur un système d’exploitation, mais vous essayez d’accéder à la page à partir de l’autre système d’exploitation. Bien que les systèmes d’exploitation puissent partager des répertoires et des fichiers, les informations de Registre utilisées par Microsoft Agent ne sont pas partagées. vous devez donc installer Microsoft Agent sur le système d’exploitation que vous utilisez pour accéder aux pages Web avec le caractère.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Lorsque je tente de charger une page scriptée pour Microsoft Agent, rien ne se produit.

Cela peut se produire si l’une des conditions suivantes est présente :

-   Vérifiez les options de sécurité de votre navigateur. votre navigateur doit être défini pour permettre le chargement de ActiveX scripts et la diffusion de ActiveX contrôles.
-   Si vous accédez à des pages scriptées avec Microsoft Agent et que vous utilisez Microsoft Internet Explorer, vous devez disposer de la version 3,02 ou ultérieure (Téléchargez la dernière version d’Internet Explorer à l’adresse [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). Dans Microsoft Internet Explorer, ouvrez le menu Affichage, choisissez Options, cliquez sur l’onglet sécurité, puis activez toutes les cases à cocher de contenu actif.
-   Une applet Java sur la page peut également provoquer cette erreur. L’exécution de Microsoft Agent sur la même page qu’une applet Java nécessite la version 2,0 de la machine virtuelle Microsoft. Pour plus d’informations, consultez le [Forum aux questions sur la programmation et l’écriture de scripts](programming-scripting-faq.yml).

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Lorsque je tente de charger une page scriptée pour Microsoft Agent, j’obtiens le message « Impossible d’initialiser Microsoft Agent ».

Cela se produit généralement lorsque vous ne disposez pas de Microsoft agent ou d’un autre contrôle sur lequel la page est installée, et que vous choisissez non lorsque vous êtes invité à installer le contrôle. Essayez d’actualiser la page, même si la page peut fonctionner uniquement si vous installez tous les composants dont elle a besoin.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Lorsque je tente de charger une page scriptée pour Microsoft Agent, j’obtiens le message « le composant a été signé numériquement » par son éditeur, mais la signature ne correspond pas au composant. Ce composant a peut-être été endommagé ou falsifié ? Voulez-vous continuer ? ».

Cela peut se produire si vous tentez d’installer Microsoft Agent sur Microsoft Internet Explorer 3,02. Vous pouvez soit poursuivre l’installation, soit mettre à jour votre navigateur vers Internet Explorer 4,0 ou version ultérieure.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Lorsque je tente de charger une page scriptée pour Microsoft Agent à l’aide de Netscape Navigator (ou d’autres navigateurs Internet), j’obtiens des erreurs.

Microsoft Agent est implémenté à l’aide d’interfaces ActiveX. vous pouvez l’utiliser uniquement avec un navigateur (tel que Microsoft Internet Explorer) qui prend en charge l’incorporation d’objets ActiveX par le biais d’un script sur une page, et uniquement sur les systèmes exécutant Microsoft Windows 95, Windows 98 et Windows NT 4,0 (ou version ultérieure). si vous n’utilisez pas Microsoft Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ), contactez le fournisseur de votre navigateur pour plus d’informations sur la prise en charge de ActiveX.

 

 




