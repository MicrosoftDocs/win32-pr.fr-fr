---
title: Objet AudioOutput
description: Objet AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381952"
---
# <a name="the-audiooutput-object"></a><span data-ttu-id="257fa-103">Objet AudioOutput</span><span class="sxs-lookup"><span data-stu-id="257fa-103">The AudioOutput Object</span></span>

<span data-ttu-id="257fa-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="257fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="257fa-105">Cet objet permet d’accéder aux propriétés de sortie audio gérées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="257fa-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="257fa-106">Les propriétés sont en lecture seule, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="257fa-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="257fa-107">Si vous déclarez une variable objet de type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), vous ne pourrez pas accéder à toutes les propriétés de l’objet [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) .</span><span class="sxs-lookup"><span data-stu-id="257fa-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="257fa-108">Tandis que agent prend également en charge [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), cette dernière interface est fournie uniquement à des fins de compatibilité descendante et prend en charge uniquement les propriétés des versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="257fa-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="257fa-109">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="257fa-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="257fa-110">**SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="257fa-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="257fa-111">**Statu**</span><span class="sxs-lookup"><span data-stu-id="257fa-111">**Status**</span></span>](status-property.md)

 

 