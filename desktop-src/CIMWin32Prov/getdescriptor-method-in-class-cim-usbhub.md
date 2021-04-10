---
description: La méthode GetDescriptor retourne le descripteur de concentrateur USB comme spécifié par les paramètres d’entrée.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Méthode GetDescriptor de la classe CIM_USBHub (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950558"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a><span data-ttu-id="f13b8-103">Méthode GetDescriptor de la \_ classe Usbhub CIM</span><span class="sxs-lookup"><span data-stu-id="f13b8-103">GetDescriptor method of the CIM\_USBHub class</span></span>

<span data-ttu-id="f13b8-104">La méthode **GetDescriptor** retourne le descripteur de concentrateur USB comme spécifié par les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f13b8-104">The **GetDescriptor** method returns the USB hub descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f13b8-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f13b8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f13b8-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f13b8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f13b8-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f13b8-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f13b8-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f13b8-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f13b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f13b8-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="f13b8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f13b8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f13b8-111">*RequestType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f13b8-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f13b8-112">Identificateur mappé en bits pour le type de demande de descripteur et le destinataire.</span><span class="sxs-lookup"><span data-stu-id="f13b8-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="f13b8-113">Pour obtenir les valeurs appropriées pour chaque bit, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="f13b8-113">For the appropriate values for each bit, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="f13b8-114">*RequestValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f13b8-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f13b8-115">Contient le type de descripteur dans l’octet de poids fort et l’index de descripteur (par exemple, index ou offset dans le tableau de descripteurs) dans l’octet de poids faible.</span><span class="sxs-lookup"><span data-stu-id="f13b8-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="f13b8-116">Pour plus d’informations, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="f13b8-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="f13b8-117">*RequestIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f13b8-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f13b8-118">Spécifie le code de l’identificateur de langue à 2 octets utilisé par le périphérique USB lors du retour de données de descripteur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="f13b8-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="f13b8-119">Le paramètre est généralement 0 (zéro) pour les descripteurs de non-chaîne.</span><span class="sxs-lookup"><span data-stu-id="f13b8-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="f13b8-120">Pour plus d’informations, consultez la spécification USB.</span><span class="sxs-lookup"><span data-stu-id="f13b8-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="f13b8-121">*RequestLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f13b8-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f13b8-122">En entrée, longueur (en octets) du descripteur qui doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="f13b8-122">On input, the length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="f13b8-123">Si cette valeur est inférieure à la longueur réelle du descripteur, seule la longueur demandée est retournée.</span><span class="sxs-lookup"><span data-stu-id="f13b8-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="f13b8-124">Si elle est supérieure à la longueur réelle, la longueur réelle est retournée.</span><span class="sxs-lookup"><span data-stu-id="f13b8-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="f13b8-125">Sur la sortie, la longueur (en octets) de la mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="f13b8-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="f13b8-126">Si le descripteur demandé n’existe pas, le contenu de ce paramètre n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f13b8-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="f13b8-127">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f13b8-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f13b8-128">La mémoire tampon retourne les informations de descripteur demandées.</span><span class="sxs-lookup"><span data-stu-id="f13b8-128">Buffer returns the requested descriptor information.</span></span> <span data-ttu-id="f13b8-129">Si le descripteur n’existe pas, le contenu de la mémoire tampon n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f13b8-129">If the descriptor does not exist, the contents of the buffer are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f13b8-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f13b8-130">Return value</span></span>

<span data-ttu-id="f13b8-131">Retourne la valeur 0 (zéro) si le descripteur USB est retourné avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f13b8-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="f13b8-132">Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="f13b8-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f13b8-133">Les chaînes dans lesquelles le contenu **mofqualifier** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="f13b8-133">The strings to which the **mofqualifier** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="f13b8-134">Notes</span><span class="sxs-lookup"><span data-stu-id="f13b8-134">Remarks</span></span>

<span data-ttu-id="f13b8-135">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="f13b8-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f13b8-136">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f13b8-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f13b8-137">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f13b8-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f13b8-138">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f13b8-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f13b8-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f13b8-139">Requirements</span></span>



| <span data-ttu-id="f13b8-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f13b8-140">Requirement</span></span> | <span data-ttu-id="f13b8-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="f13b8-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f13b8-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f13b8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f13b8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f13b8-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f13b8-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f13b8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f13b8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f13b8-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f13b8-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f13b8-146">Namespace</span></span><br/>                | <span data-ttu-id="f13b8-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f13b8-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f13b8-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="f13b8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f13b8-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f13b8-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="f13b8-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f13b8-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f13b8-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f13b8-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f13b8-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f13b8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f13b8-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f13b8-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f13b8-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f13b8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13b8-155">**\_Usbhub CIM**</span><span class="sxs-lookup"><span data-stu-id="f13b8-155">**CIM\_USBHub**</span></span>](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[<span data-ttu-id="f13b8-156">**\_Usbhub CIM**</span><span class="sxs-lookup"><span data-stu-id="f13b8-156">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> </dl>

 

