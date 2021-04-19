---
title: Player. playerApplication
description: La propriété playerApplication récupère l’objet PlayerApplication lorsqu’un contrôle du lecteur Windows Media distant est en cours d’exécution.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Lecteur Windows Media Player. playerApplication
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522798"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="521e1-104">Player. playerApplication</span><span class="sxs-lookup"><span data-stu-id="521e1-104">Player.playerApplication</span></span>

<span data-ttu-id="521e1-105">La propriété **playerApplication** récupère l’objet **playerApplication** lorsqu’un contrôle du lecteur Windows Media distant est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="521e1-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="521e1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="521e1-106">Syntax</span></span>

<span data-ttu-id="521e1-107">**playerApplication**</span><span class="sxs-lookup"><span data-stu-id="521e1-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="521e1-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="521e1-108">Possible Values</span></span>

<span data-ttu-id="521e1-109">Cette propriété est un objet **PlayerApplication** en lecture seule ou la valeur null.</span><span class="sxs-lookup"><span data-stu-id="521e1-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="521e1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="521e1-110">Remarks</span></span>

<span data-ttu-id="521e1-111">Cette propriété est utilisée uniquement lors de la communication à distance de Windows Media playercontrol.</span><span class="sxs-lookup"><span data-stu-id="521e1-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="521e1-112">Si la valeur est null, le playercontrol Windows Media n’est pas incorporé en mode distant.</span><span class="sxs-lookup"><span data-stu-id="521e1-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="521e1-113">Cette propriété est accessible uniquement dans le code C++ ou dans le code de script des habillages via la variable globale playerApplication.</span><span class="sxs-lookup"><span data-stu-id="521e1-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="521e1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="521e1-114">Requirements</span></span>



| <span data-ttu-id="521e1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="521e1-115">Requirement</span></span> | <span data-ttu-id="521e1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="521e1-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="521e1-117">Version</span><span class="sxs-lookup"><span data-stu-id="521e1-117">Version</span></span><br/> | <span data-ttu-id="521e1-118">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="521e1-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="521e1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="521e1-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="521e1-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="521e1-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="521e1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="521e1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="521e1-122">**Attributs globaux**</span><span class="sxs-lookup"><span data-stu-id="521e1-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="521e1-123">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="521e1-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="521e1-124">**Objet PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="521e1-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="521e1-125">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="521e1-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





