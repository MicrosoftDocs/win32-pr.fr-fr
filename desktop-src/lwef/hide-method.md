---
title: Hide, méthode
description: Hide, méthode
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101565"
---
# <a name="hide-method"></a><span data-ttu-id="30cd7-103">Hide, méthode</span><span class="sxs-lookup"><span data-stu-id="30cd7-103">Hide Method</span></span>

<span data-ttu-id="30cd7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30cd7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="30cd7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="30cd7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="30cd7-106">Masque le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="30cd7-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="30cd7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="30cd7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="30cd7-108">\*agent ***. Caractères («*** CharacterID \* \* * »). Masquer* \*  \[ *rapidement*\]</span><span class="sxs-lookup"><span data-stu-id="30cd7-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="30cd7-109">Partie</span><span class="sxs-lookup"><span data-stu-id="30cd7-109">Part</span></span>   | <span data-ttu-id="30cd7-110">Description</span><span class="sxs-lookup"><span data-stu-id="30cd7-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cd7-111">*Rapide*</span><span class="sxs-lookup"><span data-stu-id="30cd7-111">*Fast*</span></span> | <span data-ttu-id="30cd7-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="30cd7-112">Optional.</span></span> <span data-ttu-id="30cd7-113">Valeur booléenne qui indique s’il faut ignorer l’animation associée à l’état de masquage du caractère **true** ne joue pas l’animation de **masquage** .</span><span class="sxs-lookup"><span data-stu-id="30cd7-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="30cd7-114">**False** (valeur par défaut) lit l’animation de **masquage** .</span><span class="sxs-lookup"><span data-stu-id="30cd7-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30cd7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="30cd7-115">Remarks</span></span>

<span data-ttu-id="30cd7-116">Le serveur met en file d’attente les actions de la méthode **Hide** dans la file d’attente du caractère. vous pouvez donc l’utiliser pour masquer le caractère après une séquence d’autres animations.</span><span class="sxs-lookup"><span data-stu-id="30cd7-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="30cd7-117">Vous pouvez exécuter l’action immédiatement à l’aide de la méthode [**Stop**](stop-method.md) avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="30cd7-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="30cd7-118">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="30cd7-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="30cd7-119">En outre, si l’animation de **masquage** associée n’a pas été chargée et que vous n’avez pas spécifié le paramètre **Fast** comme **true**, le serveur définit la propriété [**État**](status-property.md) de l’objet de la **demande** sur « failed » avec un numéro d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="30cd7-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="30cd7-120">Par conséquent, si vous utilisez le protocole HTTP pour accéder à des données de caractère ou d’animation, utilisez la méthode d' [**extraction**](get-method.md) et spécifiez l’état de **masquage** pour charger l’animation avant d’appeler la méthode **Hide** .</span><span class="sxs-lookup"><span data-stu-id="30cd7-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="30cd7-121">Le masquage d’un caractère peut également entraîner le déclenchement de l’événement [**ActivateInput**](activateinput-event.md) d’un autre client.</span><span class="sxs-lookup"><span data-stu-id="30cd7-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="30cd7-122">Les caractères masqués ne peuvent pas accéder au canal audio.</span><span class="sxs-lookup"><span data-stu-id="30cd7-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="30cd7-123">Le serveur renvoie un état d’échec dans l’événement [**RequestComplete**](requestcomplete-event.md) si vous générez une demande d’animation et que le caractère est masqué.</span><span class="sxs-lookup"><span data-stu-id="30cd7-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="30cd7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30cd7-124">See Also</span></span>

[<span data-ttu-id="30cd7-125">**Show (méthode)**</span><span class="sxs-lookup"><span data-stu-id="30cd7-125">**Show method**</span></span>](show-method.md)


 

