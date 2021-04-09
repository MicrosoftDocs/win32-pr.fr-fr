---
title: Événement AgentPropertyChange
description: Événement AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028992"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="103a4-103">Événement AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="103a4-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="103a4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="103a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="103a4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="103a4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="103a4-106">Se produit lorsque l’utilisateur modifie une propriété dans la fenêtre Options de caractères avancés.</span><span class="sxs-lookup"><span data-stu-id="103a4-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="103a4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="103a4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="103a4-108">**Sous** - *agent. \* \* \* AgentPropertyChange*\*</span><span class="sxs-lookup"><span data-stu-id="103a4-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="103a4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="103a4-109">Remarks</span></span>

<span data-ttu-id="103a4-110">Cet événement indique que l’utilisateur a modifié et appliqué une propriété incluse dans la fenêtre Options de caractères avancés.</span><span class="sxs-lookup"><span data-stu-id="103a4-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="103a4-111">Dans votre code, pour gérer cet événement, vous pouvez interroger les paramètres de propriété spécifiques des objets [AudioOutput](the-audiooutput-object.md) ou [SpeechInput](the-speechinput-object.md) .</span><span class="sxs-lookup"><span data-stu-id="103a4-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="103a4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="103a4-112">See Also</span></span>

[<span data-ttu-id="103a4-113">**Événement DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="103a4-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




