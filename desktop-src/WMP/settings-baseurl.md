---
title: Paramètres. baseURL
description: La propriété baseURL spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec les commandes de script d’URL incorporées dans les éléments multimédias.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Windows Media Player Settings. baseURL
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530406"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="49f30-104">Paramètres. baseURL</span><span class="sxs-lookup"><span data-stu-id="49f30-104">Settings.baseURL</span></span>

<span data-ttu-id="49f30-105">La propriété **baseURL** spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec les commandes de script d’URL incorporées dans les éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="49f30-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f30-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49f30-106">Syntax</span></span>

<span data-ttu-id="49f30-107">Player. Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="49f30-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="49f30-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="49f30-108">Possible Values</span></span>

<span data-ttu-id="49f30-109">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="49f30-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49f30-110">Notes</span><span class="sxs-lookup"><span data-stu-id="49f30-110">Remarks</span></span>

<span data-ttu-id="49f30-111">Cette propriété spécifie l’URL HTTP de base qui est transmise en tant que paramètre de commande par l’événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="49f30-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="49f30-112">L’URL de base est concaténée avec l’URL relative, comme suit :</span><span class="sxs-lookup"><span data-stu-id="49f30-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="49f30-113">Une barre oblique finale (/) est ajoutée à la valeur de la propriété **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="49f30-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="49f30-114">Un point de début, une barre oblique inverse ou une barre oblique (., \\ et/) sont supprimés de l’URL relative.</span><span class="sxs-lookup"><span data-stu-id="49f30-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="49f30-115">L’URL relative est ajoutée à la fin de l’URL de base.</span><span class="sxs-lookup"><span data-stu-id="49f30-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="49f30-116">Toutes les barres obliques de l’URL complète résultante sont pointées dans la même direction (converties en barres obliques ou en arrière) en fonction de la direction de la première barre oblique rencontrée dans la nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="49f30-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="49f30-117">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="49f30-117">**Note**</span></span>

<span data-ttu-id="49f30-118">Le contrôle de lecteur ne prend pas en charge l’utilisation de deux points (..) dans l’URL relative pour indiquer le parent de l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="49f30-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="49f30-119">**Windows Media Player 10 Mobile**: cette propriété est en lecture seule et retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="49f30-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f30-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49f30-120">Requirements</span></span>



| <span data-ttu-id="49f30-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49f30-121">Requirement</span></span> | <span data-ttu-id="49f30-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="49f30-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49f30-123">Version</span><span class="sxs-lookup"><span data-stu-id="49f30-123">Version</span></span><br/> | <span data-ttu-id="49f30-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="49f30-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="49f30-125">DLL</span><span class="sxs-lookup"><span data-stu-id="49f30-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="49f30-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49f30-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f30-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49f30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f30-128">**Événement Player. commande**</span><span class="sxs-lookup"><span data-stu-id="49f30-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="49f30-129">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="49f30-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





