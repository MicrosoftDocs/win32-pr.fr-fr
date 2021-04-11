---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310050"
---
# <a name="iagent"></a><span data-ttu-id="a27bf-103">IAgent</span><span class="sxs-lookup"><span data-stu-id="a27bf-103">IAgent</span></span>

<span data-ttu-id="a27bf-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a27bf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a27bf-105">**IAgent** définit une interface qui permet aux applications de charger des caractères, de recevoir des événements et de vérifier l’état actuel du serveur Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a27bf-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="a27bf-106">Ces fonctions sont également disponibles à partir de [**IAgentEx**](iagentex.md).</span><span class="sxs-lookup"><span data-stu-id="a27bf-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="a27bf-107">La méthode GetSuspended incluse dans les versions précédentes est obsolète et retourne **false** pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="a27bf-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="a27bf-108">**Méthodes dans l'ordre Vtable**</span><span class="sxs-lookup"><span data-stu-id="a27bf-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="a27bf-109">Méthodes IAgent</span><span class="sxs-lookup"><span data-stu-id="a27bf-109">IAgent Methods</span></span>                               | <span data-ttu-id="a27bf-110">Description</span><span class="sxs-lookup"><span data-stu-id="a27bf-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="a27bf-111">**Load**</span><span class="sxs-lookup"><span data-stu-id="a27bf-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="a27bf-112">Charge le fichier de données d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="a27bf-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="a27bf-113">**Décharger**</span><span class="sxs-lookup"><span data-stu-id="a27bf-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="a27bf-114">Décharge le fichier de données d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="a27bf-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="a27bf-115">**S’inscrire**</span><span class="sxs-lookup"><span data-stu-id="a27bf-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="a27bf-116">Inscrit un récepteur de notification pour le client.</span><span class="sxs-lookup"><span data-stu-id="a27bf-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="a27bf-117">**Unegister**</span><span class="sxs-lookup"><span data-stu-id="a27bf-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="a27bf-118">Annule l’inscription du récepteur de notification d’un client.</span><span class="sxs-lookup"><span data-stu-id="a27bf-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="a27bf-119">**GetCharacter**</span><span class="sxs-lookup"><span data-stu-id="a27bf-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="a27bf-120">Retourne l’interface IAgentCharacter pour un caractère chargé.</span><span class="sxs-lookup"><span data-stu-id="a27bf-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 




