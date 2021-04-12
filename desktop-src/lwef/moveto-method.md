---
title: MoveTo, méthode
description: MoveTo, méthode
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031241"
---
# <a name="moveto-method"></a><span data-ttu-id="a8915-103">MoveTo, méthode</span><span class="sxs-lookup"><span data-stu-id="a8915-103">MoveTo Method</span></span>

<span data-ttu-id="a8915-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8915-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a8915-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="a8915-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a8915-106">Déplace le caractère spécifié vers l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a8915-106">Moves the specified character to the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="a8915-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="a8915-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a8915-108">\*agent ***. Caractères («*** CharacterID \* \* * »). MoveTo* \*  *x, y* \[ *Vitesse*\]</span><span class="sxs-lookup"><span data-stu-id="a8915-108">*agent ***.Characters ("*** CharacterID\*\*\*").MoveTo*\* *x,y*\[*Speed*\]</span></span>



| <span data-ttu-id="a8915-109">Partie</span><span class="sxs-lookup"><span data-stu-id="a8915-109">Part</span></span>    | <span data-ttu-id="a8915-110">Description</span><span class="sxs-lookup"><span data-stu-id="a8915-110">Description</span></span>                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8915-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="a8915-111">*x,y*</span></span>   | <span data-ttu-id="a8915-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a8915-112">Required.</span></span> <span data-ttu-id="a8915-113">Valeur entière qui indique le bord gauche (*x*) et le bord supérieur (*y*) du frame d’animation.</span><span class="sxs-lookup"><span data-stu-id="a8915-113">An integer value that indicates the left edge (*x*) and top edge (*y*) of the animation frame.</span></span> <span data-ttu-id="a8915-114">Exprimez ces coordonnées en pixels.</span><span class="sxs-lookup"><span data-stu-id="a8915-114">Express these coordinates in pixels.</span></span>                                                   |
| <span data-ttu-id="a8915-115">*Vitesse*</span><span class="sxs-lookup"><span data-stu-id="a8915-115">*Speed*</span></span> | <span data-ttu-id="a8915-116">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a8915-116">Optional.</span></span> <span data-ttu-id="a8915-117">Valeur de type entier long spécifiant, en millisecondes, la vitesse de déplacement du cadre du caractère.</span><span class="sxs-lookup"><span data-stu-id="a8915-117">A Long integer value specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="a8915-118">La valeur par défaut est 1000.</span><span class="sxs-lookup"><span data-stu-id="a8915-118">The default value is 1000.</span></span> <span data-ttu-id="a8915-119">Si vous spécifiez zéro (0), le frame est déplacé sans qu’une animation ne soit lue.</span><span class="sxs-lookup"><span data-stu-id="a8915-119">Specifying zero (0) moves the frame without playing an animation.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8915-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a8915-120">Remarks</span></span>

<span data-ttu-id="a8915-121">Le serveur lit automatiquement l’animation appropriée assignée aux États **mobiles** .</span><span class="sxs-lookup"><span data-stu-id="a8915-121">The server automatically plays the appropriate animation assigned to the **Moving** states.</span></span> <span data-ttu-id="a8915-122">L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre.</span><span class="sxs-lookup"><span data-stu-id="a8915-122">The location of a character is based on the upper left corner of its frame.</span></span>

<span data-ttu-id="a8915-123">Si vous déclarez une variable objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="a8915-123">If you declare an object variable and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="a8915-124">En outre, si l’animation associée n’a pas été chargée sur l’ordinateur local, le serveur définit la propriété d' [**État**](status-property.md) de l’objet de **requête** sur « failed » avec un numéro d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="a8915-124">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="a8915-125">Par conséquent, si vous utilisez le protocole HTTP pour accéder à des données de caractère ou d’animation, utilisez la méthode d' [**extraction**](get-method.md) pour charger les animations d’état de **déplacement** avant d’appeler la méthode **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="a8915-125">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method to load the **Moving** state animations before calling the **MoveTo** method.</span></span>

<span data-ttu-id="a8915-126">Même si l’animation n’est pas chargée, le serveur déplace toujours le frame.</span><span class="sxs-lookup"><span data-stu-id="a8915-126">Even if the animation is not loaded, the server still moves the frame.</span></span>

> [!Note]  
> <span data-ttu-id="a8915-127">Si vous appelez **MoveTo** avec une valeur différente de zéro avant que le caractère ne soit affiché, un état d’échec est retourné si vous lui avez assigné un objet de [**requête**](/windows/desktop/lwef/the-request-object) , car la valeur différente de zéro indique que vous tentez de lire une animation lorsque le caractère n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="a8915-127">If you call **MoveTo** with a nonzero value before the character is shown, it will return a failure status if you assigned it a [**Request**](/windows/desktop/lwef/the-request-object) object, because the nonzero value indicates that you are attempting to play an animation when the character is not visible.</span></span>

 

> [!Note]  
> <span data-ttu-id="a8915-128">L’effet réel du paramètre de *Vitesse* peut varier en fonction de la vitesse du processeur de l’ordinateur et de la priorité des autres tâches en cours d’exécution sur le système.</span><span class="sxs-lookup"><span data-stu-id="a8915-128">The *Speed* parameter's actual effect may vary based on the speed of the processor of the computer and the priority of other tasks running on the system.</span></span>

 

 

 