---
title: Show, méthode
description: Show, méthode
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106513708"
---
# <a name="show-method"></a><span data-ttu-id="12940-103">Show, méthode</span><span class="sxs-lookup"><span data-stu-id="12940-103">Show Method</span></span>

<span data-ttu-id="12940-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12940-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="12940-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="12940-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="12940-106">Rend le caractère spécifié visible et lit l’animation **qui lui** est associée.</span><span class="sxs-lookup"><span data-stu-id="12940-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="12940-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="12940-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="12940-108">\*agent ***. Caractères («*** CharacterID \* \* * »). Afficher* \*  \[ *rapidement*\]</span><span class="sxs-lookup"><span data-stu-id="12940-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="12940-109">Partie</span><span class="sxs-lookup"><span data-stu-id="12940-109">Part</span></span>   | <span data-ttu-id="12940-110">Description</span><span class="sxs-lookup"><span data-stu-id="12940-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12940-111">*Rapide*</span><span class="sxs-lookup"><span data-stu-id="12940-111">*Fast*</span></span> | <span data-ttu-id="12940-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="12940-112">Optional.</span></span> <span data-ttu-id="12940-113">Expression booléenne spécifiant si le serveur lit l’animation d' **affichage** .</span><span class="sxs-lookup"><span data-stu-id="12940-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="12940-114">**True** Ignore l’animation de l’état d' **émission** .</span><span class="sxs-lookup"><span data-stu-id="12940-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="12940-115">**False** (valeur par défaut) n’ignore pas l’animation de l’état d' **émission** .</span><span class="sxs-lookup"><span data-stu-id="12940-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12940-116">Notes</span><span class="sxs-lookup"><span data-stu-id="12940-116">Remarks</span></span>

<span data-ttu-id="12940-117">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="12940-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="12940-118">En outre, si **l’animation associée** n’a pas été chargée et que vous n’avez pas spécifié le paramètre **Fast** comme **true**, le serveur définit la propriété [**Status**](status-property.md) de l’objet **Request** sur « failed » avec un numéro d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="12940-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="12940-119">Par conséquent, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' [**extraction**](get-method.md) pour charger l’animation de l’état d' **affichage** avant d’appeler la méthode **Show** .</span><span class="sxs-lookup"><span data-stu-id="12940-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="12940-120">Évitez d’affecter la **valeur true** au paramètre **Fast** sans avoir préalablement lu une animation. dans le cas contraire, le frame de caractère peut s’afficher sans image.</span><span class="sxs-lookup"><span data-stu-id="12940-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="12940-121">En particulier, Notez que si vous appelez [**MoveTo**](moveto-method.md) alors que le caractère n’est pas visible, aucune animation n’est lue.</span><span class="sxs-lookup"><span data-stu-id="12940-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="12940-122">Par conséquent, si vous appelez la méthode **Show** avec **fastd** défini sur **true**, aucune image ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="12940-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="12940-123">De même, si vous appelez la fonction [**Hide**](hide-method.md) puis **Show** avec **Fast** Set à **true**, aucune image n’est visible.</span><span class="sxs-lookup"><span data-stu-id="12940-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="12940-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12940-124">See Also</span></span>

[<span data-ttu-id="12940-125">**Hide (méthode)**</span><span class="sxs-lookup"><span data-stu-id="12940-125">**Hide method**</span></span>](hide-method.md)


 

