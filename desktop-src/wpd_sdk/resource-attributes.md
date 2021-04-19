---
description: Appareils mobiles Windows prend en charge les attributs de ressource suivants.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Attributs de ressource (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537640"
---
# <a name="resource-attributes"></a><span data-ttu-id="b3578-103">Attributs de ressource</span><span class="sxs-lookup"><span data-stu-id="b3578-103">Resource Attributes</span></span>

<span data-ttu-id="b3578-104">Appareils mobiles Windows prend en charge les attributs de ressource suivants.</span><span class="sxs-lookup"><span data-stu-id="b3578-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="b3578-105">Ces attributs sont retournés par les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3578-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="b3578-106">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="b3578-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="b3578-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="b3578-107">Attribute</span></span>                                                  | <span data-ttu-id="b3578-108">VarType</span><span class="sxs-lookup"><span data-stu-id="b3578-108">VarType</span></span>      | <span data-ttu-id="b3578-109">Description</span><span class="sxs-lookup"><span data-stu-id="b3578-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3578-110">**l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="b3578-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="b3578-111">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b3578-111">**VT\_BOOL**</span></span> | <span data-ttu-id="b3578-112">Valeur booléenne qui spécifie si un client a l’autorisation de supprimer la ressource.</span><span class="sxs-lookup"><span data-stu-id="b3578-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="b3578-113">Si elle est absente, elle est supposée avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="b3578-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="b3578-114">**l' \_ attribut de ressource wpd \_ \_ peut \_ lire**</span><span class="sxs-lookup"><span data-stu-id="b3578-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="b3578-115">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b3578-115">**VT\_BOOL**</span></span> | <span data-ttu-id="b3578-116">Valeur booléenne qui spécifie si un client est autorisé à ouvrir la ressource pour l’accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="b3578-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="b3578-117">Si elle est absente, elle est supposée avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="b3578-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="b3578-118">**l' \_ attribut de ressource wpd \_ \_ peut \_ écrire**</span><span class="sxs-lookup"><span data-stu-id="b3578-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="b3578-119">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b3578-119">**VT\_BOOL**</span></span> | <span data-ttu-id="b3578-120">Valeur booléenne qui spécifie si un client est autorisé à ouvrir la ressource pour l’accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="b3578-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="b3578-121">Si elle est absente, elle est supposée avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="b3578-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="b3578-122">**\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd**</span><span class="sxs-lookup"><span data-stu-id="b3578-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="b3578-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b3578-123">**VT\_UI4**</span></span>  | <span data-ttu-id="b3578-124">Taille de mémoire tampon recommandée qu’un appelant doit utiliser pour les lectures mises en mémoire tampon à partir de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b3578-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="b3578-125">**\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd**</span><span class="sxs-lookup"><span data-stu-id="b3578-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="b3578-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="b3578-126">**VT\_UI4**</span></span>  | <span data-ttu-id="b3578-127">Taille de mémoire tampon recommandée qu’un appelant doit utiliser pour les écritures mises en mémoire tampon sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="b3578-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="b3578-128">**\_ \_ \_ taille totale de l’attribut de ressource wpd \_**</span><span class="sxs-lookup"><span data-stu-id="b3578-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="b3578-129">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="b3578-129">**VT\_UI8**</span></span>  | <span data-ttu-id="b3578-130">Taille totale des données de ressource, en octets.</span><span class="sxs-lookup"><span data-stu-id="b3578-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="b3578-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3578-131">Requirements</span></span>



| <span data-ttu-id="b3578-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3578-132">Requirement</span></span> | <span data-ttu-id="b3578-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3578-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3578-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3578-134">Header</span></span><br/> | <dl> <span data-ttu-id="b3578-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3578-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3578-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3578-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3578-137">**Propriétés**</span><span class="sxs-lookup"><span data-stu-id="b3578-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




