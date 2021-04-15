---
title: Windows 8.1 et compatibilité du client et du serveur Windows Server 2012 R2
description: Windows 8.1 et compatibilité du client et du serveur Windows Server 2012 R2
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507127"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="480ad-103">Windows 8.1 et compatibilité du client et du serveur Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="480ad-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="480ad-104">Cette section décrit les modifications apportées au système d’exploitation dont vous devez prêter une attention particulière en raison des impacts potentiels sur les applications existantes et de la façon dont les nouvelles applications doivent être conçues sur les clients, sur les serveurs, ou sur les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="480ad-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="480ad-105">Voici la liste des rubriques traitées dans cette section :</span><span class="sxs-lookup"><span data-stu-id="480ad-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="480ad-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="480ad-106">In this section</span></span>



| <span data-ttu-id="480ad-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="480ad-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="480ad-108">Description</span><span class="sxs-lookup"><span data-stu-id="480ad-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="480ad-109">Modifications apportées à la version du système d’exploitation dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="480ad-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="480ad-110">Composants Windows installés à la demande</span><span class="sxs-lookup"><span data-stu-id="480ad-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="480ad-111">Comportement de substitution de la police HTML</span><span class="sxs-lookup"><span data-stu-id="480ad-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="480ad-112">Windows 8.1 autorise uniquement les URI https, pas les URI http</span><span class="sxs-lookup"><span data-stu-id="480ad-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="480ad-113">Entrée MouseWheel pour Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="480ad-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="480ad-114">Périphériques Windows Precision Touchpad</span><span class="sxs-lookup"><span data-stu-id="480ad-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="480ad-115">Haute résolution pour les applications de bureau dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="480ad-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="480ad-116">L’interface utilisateur Edge est supprimée dans les scénarios in-out et inertie</span><span class="sxs-lookup"><span data-stu-id="480ad-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="480ad-117">L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge</span><span class="sxs-lookup"><span data-stu-id="480ad-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="480ad-118">Modèle mode IME remplacé par utilisateur par thread</span><span class="sxs-lookup"><span data-stu-id="480ad-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="480ad-119">Les API du gestionnaire de méthode d’entrée ne sont pas prises en charge par l’éditeur IME chinois simplifié</span><span class="sxs-lookup"><span data-stu-id="480ad-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="480ad-120">Certains panneaux de saisie de logiciel IME pour l’Asie de l’est envoient désormais vKey</span><span class="sxs-lookup"><span data-stu-id="480ad-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 





