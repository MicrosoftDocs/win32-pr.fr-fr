---
title: Objet SpeechInput
description: Objet SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940118"
---
# <a name="the-speechinput-object"></a><span data-ttu-id="0019a-103">Objet SpeechInput</span><span class="sxs-lookup"><span data-stu-id="0019a-103">The SpeechInput Object</span></span>

<span data-ttu-id="0019a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0019a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0019a-105">L’objet [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fournit l’accès aux propriétés d’entrée vocale gérées par le serveur de l’agent.</span><span class="sxs-lookup"><span data-stu-id="0019a-105">The [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) object provides access to the speech input properties maintained by the Agent server.</span></span> <span data-ttu-id="0019a-106">Les propriétés sont en lecture seule pour les applications clientes, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0019a-106">The properties are read-only for client applications, but the user can change them in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="0019a-107">Le serveur retourne des valeurs uniquement si un moteur de reconnaissance vocale compatible a été installé et est activé.</span><span class="sxs-lookup"><span data-stu-id="0019a-107">The server returns values only if a compatible speech engine has been installed and is enabled.</span></span>

<span data-ttu-id="0019a-108">Le [**moteur**](https://www.bing.com/search?q=**Engine**), les propriétés [**installées**](https://www.bing.com/search?q=**Installed**)et la [**langue**](https://www.bing.com/search?q=**Language**) ne sont plus prises en charge, mais (pour la compatibilité descendante) retournent des valeurs NULL si elles sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="0019a-108">The [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**), and [**Language**](https://www.bing.com/search?q=**Language**) properties are no longer supported, but (for backward compatibility) return null values if queried.</span></span> <span data-ttu-id="0019a-109">Pour interroger ou définir le mode d’une reconnaissance vocale, utilisez la propriété [**SRModeID**](srmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="0019a-109">To query or set a speech recognition's mode, use the [**SRModeID**](srmodeid-property.md) property.</span></span>

-   [<span data-ttu-id="0019a-110">Propriétés SpeechInput</span><span class="sxs-lookup"><span data-stu-id="0019a-110">SpeechInput Properties</span></span>](speechinput-properties.md)

 

 




