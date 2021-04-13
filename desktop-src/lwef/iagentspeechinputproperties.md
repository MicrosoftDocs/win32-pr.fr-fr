---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379564"
---
# <a name="iagentspeechinputproperties"></a><span data-ttu-id="7a7c6-103">IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="7a7c6-103">IAgentSpeechInputProperties</span></span>

<span data-ttu-id="7a7c6-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7a7c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7a7c6-105">IAgentSpeechInputProperties fournit l’accès aux propriétés d’entrée vocale gérées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-105">IAgentSpeechInputProperties provides access to the speech input properties maintained by the server.</span></span> <span data-ttu-id="7a7c6-106">La plupart des propriétés sont en lecture seule pour les applications clientes, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-106">Most of the properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="7a7c6-107">Le serveur Microsoft Agent retourne des valeurs uniquement si un moteur de reconnaissance vocale compatible a été installé et est activé.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-107">The Microsoft Agent server returns values only if a compatible speech engine has been installed and is enabled.</span></span> <span data-ttu-id="7a7c6-108">L’interrogation de ces propriétés tente de démarrer le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-108">Querying these properties attempts to start the speech engine.</span></span>

<span data-ttu-id="7a7c6-109">**Méthodes dans l'ordre Vtable**</span><span class="sxs-lookup"><span data-stu-id="7a7c6-109">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="7a7c6-110">Méthodes IAgentSpeechInputProperties</span><span class="sxs-lookup"><span data-stu-id="7a7c6-110">IAgentSpeechInputProperties Methods</span></span>                                     | <span data-ttu-id="7a7c6-111">Description</span><span class="sxs-lookup"><span data-stu-id="7a7c6-111">Description</span></span>                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="7a7c6-112">**GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="7a7c6-112">**GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)           | <span data-ttu-id="7a7c6-113">Retourne une valeur indiquant si le moteur de reconnaissance vocale est activé.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-113">Returns whether the speech recognition engine is enabled.</span></span> |
| [<span data-ttu-id="7a7c6-114">**GetHotKey**</span><span class="sxs-lookup"><span data-stu-id="7a7c6-114">**GetHotKey**</span></span>](iagentspeechinputproperties--gethotkey.md)             | <span data-ttu-id="7a7c6-115">Retourne l’affectation de clé actuelle de la clé d’écoute.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-115">Returns the current key assignment of the Listening key.</span></span>  |
| [<span data-ttu-id="7a7c6-116">**GetListeningTip**</span><span class="sxs-lookup"><span data-stu-id="7a7c6-116">**GetListeningTip**</span></span>](iagentspeechinputproperties--getlisteningtip.md) | <span data-ttu-id="7a7c6-117">Retourne une valeur indiquant si l’info-bulle d’écoute est activée.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-117">Returns whether the Listening Tip is enabled.</span></span>             |



 

<span data-ttu-id="7a7c6-118">Les méthodes [**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)et [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (prises en charge dans les versions antérieures de Microsoft Agent) sont toujours prises en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-118">[**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**), and [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) methods (supported in earlier versions of Microsoft Agent) are still supported for backward compatibility.</span></span> <span data-ttu-id="7a7c6-119">Toutefois, les méthodes ne sont pas extraites et ne retournent pas de valeurs utiles.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-119">However, the methods are not stubbed and do not return useful values.</span></span> <span data-ttu-id="7a7c6-120">Utilisez [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) et [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) pour interroger et définir le moteur de reconnaissance vocale à utiliser avec le caractère.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-120">Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) and [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) to query and set the speech recognition engine to be used with the character.</span></span> <span data-ttu-id="7a7c6-121">Gardez à l’esprit que le moteur doit correspondre au paramètre de langue actuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="7a7c6-121">Keep in mind that the engine must match the character's current language setting.</span></span>

 

 




