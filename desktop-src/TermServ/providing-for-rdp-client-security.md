---
title: Fournir la sécurité du client RDP
description: certaines propriétés de l’objet de contrôle Bureau à distance ActiveX sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008605"
---
# <a name="providing-for-rdp-client-security"></a>Fournir la sécurité du client RDP

pour permettre aux clients de se protéger eux-mêmes des serveurs potentiellement non fiables, certaines propriétés de l’objet de contrôle Bureau à distance ActiveX sont limitées à des zones de sécurité URL Internet Explorer spécifiques. Cela signifie que, quand un utilisateur naviguant sur le Web accède à la page et que la page se trouve dans une zone de sécurité d’URL supérieure à celle de l’ordinateur sur lequel il navigue sur le Web, ces propriétés sont désactivées. Ces propriétés restreintes sont accessibles à l’aide de l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) et de l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , et sont disponibles dans les zones de sécurité des URL d’Internet Explorer suivantes :

-   Mon ordinateur
-   Intranet local
-   Sites de confiance

Ils sont désactivés dans les zones suivantes :

-   Internet
-   Sites sensibles

si vous appelez ces propriétés restreintes au sein de votre application web Services Bureau à distance, vous devez appeler [**IMsTscAx :: \_ SecuredSettings**](imstscax-securedsettings.md) et [**IMsTscAx :: obten \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) pour accéder aux propriétés de Paramètres sécurisées.

Les propriétés restreintes auxquelles l’interface **IMsTscSecuredSettings** accède sont les suivantes :

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Cette propriété spécifie le programme qui sera démarré lors de la connexion.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Cette propriété spécifie le répertoire de travail du programme spécifié dans [**StartProgram**](imstscsecuredsettings-startprogram.md).
-   [**Plein écran**](imstscsecuredsettings-fullscreen.md). Cette propriété spécifie si l’état du contrôle lors de la connexion est en mode plein écran ou fenêtre. Si la valeur de cette propriété est **true**, la connexion est ouverte en mode plein écran. Bien que l’utilisation de la propriété **fullscreen** soit limitée aux zones de sécurité des URL d’Internet Explorer répertoriées précédemment, un utilisateur peut toujours passer en mode plein écran après connexion en appuyant sur la combinaison de [touches de raccourci](terminal-services-shortcut-keys.md) en mode plein écran (Ctrl + Alt + Attn).

Les propriétés auxquelles l’interface **IMsRdpClientSecuredSettings** accède sont les suivantes :

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Cette propriété spécifie s’il faut rediriger les sons ou émettre des sons sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). cette propriété spécifie comment et quand appliquer Windows combinaisons de touches ; par exemple, ALT + TAB.

Le script suivant lance Microsoft Notepad.exe lors de la connexion. exécutez ce script avant d’appeler la méthode [**IMsTscAx :: Connecter**](imstscax-connect.md) .

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




