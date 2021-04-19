---
description: Appareils mobiles Windows prend en charge les propriétés d’association de réseau suivantes.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propriétés de l’Association réseau (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524035"
---
# <a name="network-association-properties"></a><span data-ttu-id="2353f-103">Propriétés de l’Association réseau</span><span class="sxs-lookup"><span data-stu-id="2353f-103">Network Association Properties</span></span>

<span data-ttu-id="2353f-104">Appareils mobiles Windows prend en charge les propriétés d’association de réseau suivantes.</span><span class="sxs-lookup"><span data-stu-id="2353f-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="2353f-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="2353f-105">Property</span></span>                                                  | <span data-ttu-id="2353f-106">VarType</span><span class="sxs-lookup"><span data-stu-id="2353f-106">VarType</span></span>                   | <span data-ttu-id="2353f-107">Description</span><span class="sxs-lookup"><span data-stu-id="2353f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2353f-108">**\_ \_ \_ \_ identificateurs de réseau hôte d’association de réseau wpd \_**</span><span class="sxs-lookup"><span data-stu-id="2353f-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="2353f-109">**VT \_ UI1 VT Vector \| \_**</span><span class="sxs-lookup"><span data-stu-id="2353f-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="2353f-110">Liste des identificateurs d’hôte EUI-64 valides pour cette association. Il s’agit d’un tableau d’octets qui contient un nombre entier d’adresses réseau physiques EUI-64.</span><span class="sxs-lookup"><span data-stu-id="2353f-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="2353f-111">Ces valeurs EUI-64 sont les adresses réseau physiques disponibles sur l’hôte au moment de l’Association du réseau.</span><span class="sxs-lookup"><span data-stu-id="2353f-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="2353f-112">Si l’ordinateur hôte possède des adresses réseau physiques MAC-48 (par défaut des réseaux IPv4), chaque adresse MAC-48 est encodée dans l’adresse EUI-64, car les deux moitiés de l’adresse MAC-48 sont séparées par FF-FF.</span><span class="sxs-lookup"><span data-stu-id="2353f-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="2353f-113">**\_Association de réseau wpd \_ \_ X509V3SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="2353f-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="2353f-114">**VT \_ UI1 VT Vector \| \_**</span><span class="sxs-lookup"><span data-stu-id="2353f-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="2353f-115">Séquence des certificats X. 509 v3 à fournir pour l’authentification du serveur TLS.</span><span class="sxs-lookup"><span data-stu-id="2353f-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="2353f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2353f-116">Requirements</span></span>



| <span data-ttu-id="2353f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2353f-117">Requirement</span></span> | <span data-ttu-id="2353f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2353f-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2353f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2353f-119">Header</span></span><br/> | <dl> <span data-ttu-id="2353f-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2353f-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2353f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2353f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2353f-122">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="2353f-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




