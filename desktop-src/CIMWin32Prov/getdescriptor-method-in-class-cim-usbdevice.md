---
description: La méthode GetDescriptor retourne le descripteur de périphérique USB comme spécifié par les paramètres d’entrée.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Méthode GetDescriptor de la classe CIM_USBDevice (Wmcodecdsp. h)
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
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517188"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a><span data-ttu-id="1adb6-103">Méthode GetDescriptor de la classe CIM_USBDevice (Wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="1adb6-103">GetDescriptor method of the CIM_USBDevice class (Wmcodecdsp.h)</span></span>

<span data-ttu-id="1adb6-104">La méthode **GetDescriptor** retourne le descripteur de périphérique USB comme spécifié par les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1adb6-104">The **GetDescriptor** method returns the USB device descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1adb6-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1adb6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1adb6-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1adb6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1adb6-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1adb6-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1adb6-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1adb6-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1adb6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1adb6-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="1adb6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1adb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1adb6-111">*RequestType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1adb6-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1adb6-112">Identificateur mappé en bits pour le type de demande de descripteur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="1adb6-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="1adb6-113">Reportez-vous à la spécification USB pour obtenir les valeurs appropriées pour chaque bit.</span><span class="sxs-lookup"><span data-stu-id="1adb6-113">Refer to the USB specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="1adb6-114">*RequestValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1adb6-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1adb6-115">Contient le type de descripteur dans l’octet de poids fort et l’index de descripteur (par exemple, index ou offset dans le tableau de descripteurs) dans l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="1adb6-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="1adb6-116">Pour plus d’informations, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="1adb6-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="1adb6-117">*RequestIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1adb6-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1adb6-118">Spécifie le code de l’identificateur de langue à 2 octets utilisé par le périphérique USB lors du retour de données de descripteur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="1adb6-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="1adb6-119">Le paramètre est généralement 0 (zéro) pour les descripteurs de non-chaîne.</span><span class="sxs-lookup"><span data-stu-id="1adb6-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="1adb6-120">Pour plus d’informations, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="1adb6-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="1adb6-121">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1adb6-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1adb6-122">En entrée, longueur (en octets) du descripteur qui doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="1adb6-122">On input, length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="1adb6-123">Si cette valeur est inférieure à la longueur réelle du descripteur, seule la longueur demandée est retournée.</span><span class="sxs-lookup"><span data-stu-id="1adb6-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="1adb6-124">Si elle est supérieure à la longueur réelle, la longueur réelle est retournée.</span><span class="sxs-lookup"><span data-stu-id="1adb6-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="1adb6-125">Sur la sortie, la longueur (en octets) de la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="1adb6-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="1adb6-126">Si le descripteur demandé n’existe pas, le contenu de ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1adb6-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="1adb6-127">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1adb6-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1adb6-128">Retourne les informations de descripteur demandées.</span><span class="sxs-lookup"><span data-stu-id="1adb6-128">Returns the requested descriptor information.</span></span> <span data-ttu-id="1adb6-129">Si le descripteur n’existe pas, le contenu de ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1adb6-129">If the descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1adb6-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1adb6-130">Return value</span></span>

<span data-ttu-id="1adb6-131">Retourne la valeur 0 (zéro) si le descripteur USB est retourné avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1adb6-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="1adb6-132">Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="1adb6-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="1adb6-133">Les chaînes dans lesquelles le contenu mofqualifier est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="1adb6-133">The strings to which the mofqualifier contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="1adb6-134">Notes</span><span class="sxs-lookup"><span data-stu-id="1adb6-134">Remarks</span></span>

<span data-ttu-id="1adb6-135">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="1adb6-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1adb6-136">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1adb6-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1adb6-137">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1adb6-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1adb6-138">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1adb6-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1adb6-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1adb6-139">Requirements</span></span>



| <span data-ttu-id="1adb6-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1adb6-140">Requirement</span></span> | <span data-ttu-id="1adb6-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="1adb6-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1adb6-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1adb6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1adb6-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1adb6-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1adb6-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1adb6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1adb6-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1adb6-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1adb6-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1adb6-146">Namespace</span></span><br/>                | <span data-ttu-id="1adb6-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1adb6-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1adb6-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="1adb6-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1adb6-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1adb6-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1adb6-150">MOF</span><span class="sxs-lookup"><span data-stu-id="1adb6-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1adb6-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1adb6-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1adb6-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1adb6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1adb6-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1adb6-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1adb6-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1adb6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1adb6-155">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1adb6-155">**CIM\_USBDevice**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[<span data-ttu-id="1adb6-156">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1adb6-156">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

