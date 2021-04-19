---
description: La commande \_ wpd \_ Device \_ Hints \_ obtenir \_ \_ l’emplacement du contenu récupère les ID d’objet des dossiers qui peuvent contenir un objet d’un type spécifié.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Commande WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525355"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="a215c-103">Commande \_ wpd \_ Device \_ Hints \_ , \_ commande d’emplacement du contenu \_</span><span class="sxs-lookup"><span data-stu-id="a215c-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="a215c-104">La **commande \_ wpd \_ Device \_ Hints \_ obtenir \_ l' \_ emplacement du contenu** récupère les ID d’objet des dossiers qui peuvent contenir un objet d’un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="a215c-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="a215c-105">Cette commande est fournie comme un moyen plus rapide pour un client de découvrir où un appareil stocke des objets spécifiques que par l’énumération d’objets en brute.</span><span class="sxs-lookup"><span data-stu-id="a215c-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="a215c-106">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="a215c-106">Command category</span></span>

<span data-ttu-id="a215c-107">**indicateurs d’appareil de la \_ catégorie wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a215c-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="a215c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a215c-108">Parameters</span></span>

<span data-ttu-id="a215c-109">Le pilote attend les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a215c-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="a215c-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a215c-110">Parameter</span></span>                                   | <span data-ttu-id="a215c-111">VarType</span><span class="sxs-lookup"><span data-stu-id="a215c-111">VarType</span></span>   | <span data-ttu-id="a215c-112">Description</span><span class="sxs-lookup"><span data-stu-id="a215c-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a215c-113">\_type de \_ contenu des indications d’appareil \_ \_ de la propriété wpd \_</span><span class="sxs-lookup"><span data-stu-id="a215c-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="a215c-114">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="a215c-114">VT\_CLSID</span></span> | <span data-ttu-id="a215c-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a215c-115">Required.</span></span> <span data-ttu-id="a215c-116">Type d’objet pour lequel l’appelant souhaite rechercher le conteneur.</span><span class="sxs-lookup"><span data-stu-id="a215c-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="a215c-117">Par exemple, pour rechercher les dossiers de niveau supérieur utilisés pour stocker des images sur un appareil photo numérique, l’appelant doit envoyer une \_ image de type de contenu wpd \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a215c-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="a215c-118">Consultez [Configuration requise pour les objets](requirements-for-objects.md) pour obtenir la liste des types d’objets définis par les appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="a215c-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="a215c-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a215c-119">Return Value</span></span>

<span data-ttu-id="a215c-120">Le pilote doit renvoyer les résultats suivants.</span><span class="sxs-lookup"><span data-stu-id="a215c-120">The driver should return the following results.</span></span>



| <span data-ttu-id="a215c-121">Résultats</span><span class="sxs-lookup"><span data-stu-id="a215c-121">Result</span></span>                                               | <span data-ttu-id="a215c-122">VarType</span><span class="sxs-lookup"><span data-stu-id="a215c-122">VarType</span></span>     | <span data-ttu-id="a215c-123">Description</span><span class="sxs-lookup"><span data-stu-id="a215c-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a215c-124">**Propriétés WPD indicateurs de l' \_ appareil de \_ \_ \_ contenu \_**</span><span class="sxs-lookup"><span data-stu-id="a215c-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="a215c-125">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="a215c-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="a215c-126">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a215c-126">Required.</span></span> <span data-ttu-id="a215c-127">[**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de type VT \_ LPWStr qui spécifie les ID d’objet de dossiers contenant des objets du type indiqué par le paramètre appelant.</span><span class="sxs-lookup"><span data-stu-id="a215c-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="a215c-128">Si aucun dossier n’est trouvé, il doit s’agir d’une liste vide. Les dossiers indiqués par le résultat peuvent ou non contenir des objets d’autres types de contenu.</span><span class="sxs-lookup"><span data-stu-id="a215c-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="a215c-129">Pour plus d’informations sur les restrictions de dossiers, consultez la propriété [ \_ types de contenu de dossier wpd \_ \_ \_ autorisés](miscellaneous-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a215c-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="a215c-130">**\_valeur courante de la propriété wpd \_ \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a215c-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="a215c-131">\_erreur VT</span><span class="sxs-lookup"><span data-stu-id="a215c-131">VT\_ERROR</span></span>   | <span data-ttu-id="a215c-132">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a215c-132">Required.</span></span> <span data-ttu-id="a215c-133">**HRESULT** qui indique la réussite ou l’échec de la gestion de la commande.</span><span class="sxs-lookup"><span data-stu-id="a215c-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="a215c-134">Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat.</span><span class="sxs-lookup"><span data-stu-id="a215c-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="a215c-135">Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="a215c-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="a215c-136">**\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**</span><span class="sxs-lookup"><span data-stu-id="a215c-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="a215c-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="a215c-137">VT\_UI4</span></span>     | <span data-ttu-id="a215c-138">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a215c-138">Optional.</span></span> <span data-ttu-id="a215c-139">Code d’erreur spécifique au pilote.</span><span class="sxs-lookup"><span data-stu-id="a215c-139">A driver-specific error code.</span></span> <span data-ttu-id="a215c-140">Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.</span><span class="sxs-lookup"><span data-stu-id="a215c-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="a215c-141">Appel de méthodes</span><span class="sxs-lookup"><span data-stu-id="a215c-141">Calling Methods</span></span>

<span data-ttu-id="a215c-142">Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="a215c-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="a215c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a215c-143">Requirements</span></span>



| <span data-ttu-id="a215c-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a215c-144">Requirement</span></span> | <span data-ttu-id="a215c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="a215c-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a215c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="a215c-146">Header</span></span><br/> | <dl> <span data-ttu-id="a215c-147"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a215c-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




