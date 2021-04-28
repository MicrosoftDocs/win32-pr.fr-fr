---
description: Chaîne de l’agent utilisateur
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Chaîne de l’agent utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084177"
---
# <a name="user-agent-string"></a><span data-ttu-id="958ee-103">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="958ee-103">User Agent String</span></span>

<span data-ttu-id="958ee-104">La *chaîne de l’agent utilisateur* contient des informations sur l’identité d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="958ee-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="958ee-105">La chaîne de l’agent utilisateur est signalée au serveur Web en tant qu’en-tête HTTP chaque fois qu’un navigateur envoie une demande à un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="958ee-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="958ee-106">Vous pouvez également y accéder par le biais d’un script côté client.</span><span class="sxs-lookup"><span data-stu-id="958ee-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="958ee-107">Par exemple, vous pouvez afficher la chaîne de l’agent utilisateur en tapant l’URL suivante dans la barre d’adresses Windows Internet Explorer 8 : « JavaScript : Alert (Navigator. userAgent) ».</span><span class="sxs-lookup"><span data-stu-id="958ee-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="958ee-108">L’illustration suivante montre la boîte de dialogue résultante standard d’Internet Explorer 8 s’exécutant sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="958ee-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![capture d’écran de la boîte de diaog d’Internet Explorer qui contient la chaîne de l’agent utilisateur](images/useragent-alert.png)

<span data-ttu-id="958ee-110">En règle générale, la chaîne de l’agent utilisateur est analysée spécifiquement pour la sous-chaîne MSIE.</span><span class="sxs-lookup"><span data-stu-id="958ee-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="958ee-111">Selon la version signalée du navigateur, la logique de programmation côté client ou côté serveur effectue une action différente.</span><span class="sxs-lookup"><span data-stu-id="958ee-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="958ee-112">Pour plus d’informations sur la chaîne de l’agent utilisateur, voir [qu’est-ce que Windows Internet Explorer signalera comme chaîne de User-Agent ?](/previous-versions/cc817582(v=msdn.10)) dans MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="958ee-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="958ee-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="958ee-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="958ee-114">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="958ee-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



