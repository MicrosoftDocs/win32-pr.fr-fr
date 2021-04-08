---
title: Fournir la sécurité du client RDP
description: Certaines propriétés de l’objet de contrôle ActiveX Bureau à distance sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672990"
---
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="e7486-103">Fournir la sécurité du client RDP</span><span class="sxs-lookup"><span data-stu-id="e7486-103">Providing for RDP client security</span></span>

<span data-ttu-id="e7486-104">Pour permettre aux clients de se protéger eux-mêmes des serveurs potentiellement non fiables, certaines propriétés de l’objet de contrôle ActiveX Bureau à distance sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e7486-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="e7486-105">Cela signifie que, quand un utilisateur naviguant sur le Web accède à la page et que la page se trouve dans une zone de sécurité d’URL supérieure à celle de l’ordinateur sur lequel il navigue sur le Web, ces propriétés sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="e7486-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="e7486-106">Ces propriétés restreintes sont accessibles à l’aide de l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) et de l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , et sont disponibles dans les zones de sécurité des URL d’Internet Explorer suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7486-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="e7486-107">Mon ordinateur</span><span class="sxs-lookup"><span data-stu-id="e7486-107">My computer</span></span>
-   <span data-ttu-id="e7486-108">Intranet local</span><span class="sxs-lookup"><span data-stu-id="e7486-108">Local intranet</span></span>
-   <span data-ttu-id="e7486-109">Sites de confiance</span><span class="sxs-lookup"><span data-stu-id="e7486-109">Trusted sites</span></span>

<span data-ttu-id="e7486-110">Ils sont désactivés dans les zones suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7486-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="e7486-111">Internet</span><span class="sxs-lookup"><span data-stu-id="e7486-111">Internet</span></span>
-   <span data-ttu-id="e7486-112">Sites sensibles</span><span class="sxs-lookup"><span data-stu-id="e7486-112">Restricted sites</span></span>

<span data-ttu-id="e7486-113">Si vous appelez ces propriétés restreintes au sein de votre application Web Services Bureau à distance, vous devez appeler [**IMsTscAx :: \_ SecuredSettings**](imstscax-securedsettings.md) et [**IMsTscAx :: obtient \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) pour accéder aux propriétés des paramètres sécurisés.</span><span class="sxs-lookup"><span data-stu-id="e7486-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="e7486-114">Les propriétés restreintes auxquelles l’interface **IMsTscSecuredSettings** accède sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7486-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="e7486-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="e7486-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="e7486-116">Cette propriété spécifie le programme qui sera démarré lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="e7486-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="e7486-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span><span class="sxs-lookup"><span data-stu-id="e7486-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="e7486-118">Cette propriété spécifie le répertoire de travail du programme spécifié dans [**StartProgram**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="e7486-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="e7486-119">[**Plein écran**](imstscsecuredsettings-fullscreen.md).</span><span class="sxs-lookup"><span data-stu-id="e7486-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="e7486-120">Cette propriété spécifie si l’état du contrôle lors de la connexion est en mode plein écran ou fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e7486-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="e7486-121">Si la valeur de cette propriété est **true**, la connexion est ouverte en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="e7486-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="e7486-122">Bien que l’utilisation de la propriété **fullscreen** soit limitée aux zones de sécurité des URL d’Internet Explorer répertoriées précédemment, un utilisateur peut toujours passer en mode plein écran après connexion en appuyant sur la combinaison de [touches de raccourci](terminal-services-shortcut-keys.md) en mode plein écran (Ctrl + Alt + Attn).</span><span class="sxs-lookup"><span data-stu-id="e7486-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="e7486-123">Les propriétés auxquelles l’interface **IMsRdpClientSecuredSettings** accède sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7486-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="e7486-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span><span class="sxs-lookup"><span data-stu-id="e7486-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="e7486-125">Cette propriété spécifie s’il faut rediriger les sons ou émettre des sons sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="e7486-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="e7486-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span><span class="sxs-lookup"><span data-stu-id="e7486-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="e7486-127">Cette propriété spécifie comment et quand appliquer les combinaisons de touches Windows. par exemple, ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="e7486-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="e7486-128">Le script suivant lance Microsoft Notepad.exe lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="e7486-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="e7486-129">Exécutez ce script avant d’appeler la méthode [**IMsTscAx :: Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="e7486-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




