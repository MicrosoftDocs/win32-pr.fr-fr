---
title: Propriétés du contrôle de l’agent
description: Propriétés du contrôle de l’agent
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028769"
---
# <a name="agent-control-properties"></a><span data-ttu-id="a7d38-103">Propriétés du contrôle de l’agent</span><span class="sxs-lookup"><span data-stu-id="a7d38-103">Agent Control Properties</span></span>

<span data-ttu-id="a7d38-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a7d38-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a7d38-105">Les propriétés suivantes sont directement accessibles à partir du contrôle de l’agent :</span><span class="sxs-lookup"><span data-stu-id="a7d38-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="a7d38-106">**Connecté**</span><span class="sxs-lookup"><span data-stu-id="a7d38-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="a7d38-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a7d38-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="a7d38-108">**RaiseRequestErrors**</span><span class="sxs-lookup"><span data-stu-id="a7d38-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="a7d38-109">En outre, certains environnements de programmation peuvent assigner des propriétés supplémentaires au moment du design ou au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a7d38-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="a7d38-110">Par exemple, Visual Basic ajoute les propriétés gauche, index, tag et Top qui définissent l’emplacement du contrôle sur un formulaire, même si le contrôle n’apparaît pas sur la page du formulaire au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a7d38-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="a7d38-111">La propriété Suspended est toujours prise en charge pour la compatibilité descendante, mais retourne toujours **false** , car le serveur ne prend plus en charge l’État Suspended.</span><span class="sxs-lookup"><span data-stu-id="a7d38-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




