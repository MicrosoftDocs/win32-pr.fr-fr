---
title: Méthode GestureAt
description: Méthode GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462987"
---
# <a name="gestureat-method"></a><span data-ttu-id="072b1-103">Méthode GestureAt</span><span class="sxs-lookup"><span data-stu-id="072b1-103">GestureAt Method</span></span>

<span data-ttu-id="072b1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="072b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="072b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="072b1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="072b1-106">Lit l’animation gesturing pour le caractère spécifié à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="072b1-106">Plays the gesturing animation for the specified character at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="072b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="072b1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="072b1-108">\*agent ***. Caractères («*** CharacterID \* \* * »). GestureAt* \*  *x, y*</span><span class="sxs-lookup"><span data-stu-id="072b1-108">*agent ***.Characters ("*** CharacterID\*\*\*").GestureAt*\* *x,y*</span></span>



| <span data-ttu-id="072b1-109">Partie</span><span class="sxs-lookup"><span data-stu-id="072b1-109">Part</span></span>  | <span data-ttu-id="072b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="072b1-110">Description</span></span>                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="072b1-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="072b1-111">*x,y*</span></span> | <span data-ttu-id="072b1-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="072b1-112">Required.</span></span> <span data-ttu-id="072b1-113">Valeur entière qui indique la coordonnée d’écran horizontale (*x*) et la coordonnée d’écran verticale (*y*) à laquelle le caractère sera geste.</span><span class="sxs-lookup"><span data-stu-id="072b1-113">An integer value that indicates the horizontal (*x*) screen coordinate and vertical (*y*) screen coordinate to which the character will gesture.</span></span> <span data-ttu-id="072b1-114">Ces coordonnées doivent être spécifiées en pixels.</span><span class="sxs-lookup"><span data-stu-id="072b1-114">These coordinates must be specified in pixels.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="072b1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="072b1-115">Remarks</span></span>

<span data-ttu-id="072b1-116">Le serveur lit automatiquement l’animation appropriée au geste vers l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="072b1-116">The server automatically plays the appropriate animation to gesture toward the specified location.</span></span> <span data-ttu-id="072b1-117">Les coordonnées sont toujours relatives à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="072b1-117">The coordinates are always relative to the screen origin (upper left).</span></span>

<span data-ttu-id="072b1-118">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="072b1-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="072b1-119">En outre, si l’animation associée n’a pas été chargée sur l’ordinateur local, le serveur définit la propriété d' [**État**](status-property.md) de l’objet de **requête** sur « failed » avec un numéro d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="072b1-119">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="072b1-120">Par conséquent, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' [**extraction**](get-method.md) pour charger les animations d’état **gesturing** avant d’appeler la méthode **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="072b1-120">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Gesturing** state animations before calling the **GestureAt** method.</span></span>

 

 