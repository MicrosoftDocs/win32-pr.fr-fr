---
description: Retourne le descripteur USBDevice comme spécifié par les paramètres d’entrée.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Méthode GetDescriptor de la classe CIM_USBDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529780"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="9a095-103">Méthode GetDescriptor de la classe CIM_USBDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="9a095-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="9a095-104">Retourne le descripteur USBDevice comme spécifié par les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9a095-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a095-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a095-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="9a095-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a095-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a095-107">*RequestType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a095-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a095-108">Mappage de bits qui identifie le type de demande de descripteur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="9a095-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="9a095-109">Le type de la demande peut être « standard », « Class » ou « Specification Vendor ».</span><span class="sxs-lookup"><span data-stu-id="9a095-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="9a095-110">Le destinataire peut être « Device », « interface », « Endpoint » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="9a095-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="9a095-111">Reportez-vous à la spécification USB pour obtenir les valeurs appropriées pour chaque bit.</span><span class="sxs-lookup"><span data-stu-id="9a095-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="9a095-112">*RequestValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a095-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a095-113">Contient le type de descripteur dans l’octet de poids fort et l’index de descripteur (par exemple, index ou offset dans le tableau de descripteurs) dans l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="9a095-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="9a095-114">Pour plus d’informations, reportez-vous à la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="9a095-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="9a095-115">*RequestIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a095-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a095-116">Définit le code d’ID de langage de 2 octets utilisé par USBDevice lors du retour de données de descripteur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a095-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="9a095-117">Le paramètre est généralement 0 pour les descripteurs de non-chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a095-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="9a095-118">Pour plus d’informations, reportez-vous à la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="9a095-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="9a095-119">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9a095-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a095-120">En entrée, contient la longueur (en octets) du descripteur qui doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="9a095-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="9a095-121">Si cette valeur est inférieure à la longueur réelle du descripteur, seule la longueur demandée est retournée.</span><span class="sxs-lookup"><span data-stu-id="9a095-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="9a095-122">Si elle est supérieure à la longueur réelle, la longueur réelle est retournée.</span><span class="sxs-lookup"><span data-stu-id="9a095-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="9a095-123">Lors de la sortie, ce paramètre correspond à la longueur, en octets, de la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="9a095-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="9a095-124">Si le descripteur demandé n’existe pas, le contenu de ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9a095-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="9a095-125">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a095-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a095-126">Retourne les informations de descripteur demandées.</span><span class="sxs-lookup"><span data-stu-id="9a095-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="9a095-127">Si le descripteur n’existe pas, le contenu du paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9a095-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a095-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a095-128">Return value</span></span>

<span data-ttu-id="9a095-129">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="9a095-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a095-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a095-130">Requirements</span></span>



| <span data-ttu-id="9a095-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a095-131">Requirement</span></span> | <span data-ttu-id="9a095-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a095-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a095-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a095-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9a095-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9a095-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9a095-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a095-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9a095-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9a095-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9a095-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9a095-137">Namespace</span></span><br/>                | <span data-ttu-id="9a095-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9a095-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9a095-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9a095-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a095-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a095-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a095-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9a095-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a095-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a095-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a095-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a095-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a095-144">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9a095-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




