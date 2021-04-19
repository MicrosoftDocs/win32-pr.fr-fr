---
description: La fonction d’exportation AttachProperties mappe les propriétés à un emplacement dans une partie des données reconnues. AttachProperties doit être implémenté pour chaque analyseur pris en charge par la DLL de l’analyseur.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Fonction de rappel AttachProperties (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533875"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="02577-104">AttachProperties fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="02577-104">AttachProperties callback function</span></span>

<span data-ttu-id="02577-105">La fonction d’exportation **AttachProperties** mappe les propriétés à un emplacement dans une partie des données reconnues.</span><span class="sxs-lookup"><span data-stu-id="02577-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="02577-106">**AttachProperties** doit être implémenté pour chaque analyseur pris en charge par la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="02577-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="02577-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02577-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="02577-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02577-109">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-110">Handle du frame en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="02577-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="02577-111">*lpFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-112">Pointeur vers le premier octet d’un frame.</span><span class="sxs-lookup"><span data-stu-id="02577-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="02577-113">*lpProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-114">Pointeur vers le début des données reconnues.</span><span class="sxs-lookup"><span data-stu-id="02577-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="02577-115">*MacType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-116">Valeur MAC du premier protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="02577-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="02577-117">Le *paractype* peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="02577-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="02577-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="02577-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="02577-119">Signification</span><span class="sxs-lookup"><span data-stu-id="02577-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="02577-120"><dt>**MAC \_ type \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="02577-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="02577-121">802.3</span><span class="sxs-lookup"><span data-stu-id="02577-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="02577-122"><dt>**\_type Mac \_ TOKENRING**</dt></span><span class="sxs-lookup"><span data-stu-id="02577-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="02577-123">802.5</span><span class="sxs-lookup"><span data-stu-id="02577-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="02577-124"><dt>**\_type Mac \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="02577-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="02577-125">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="02577-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="02577-126">*BytesLeft* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-127">Nombre d’octets restants dans un frame à partir du début des données reconnues.</span><span class="sxs-lookup"><span data-stu-id="02577-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="02577-128">*hPreviousProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-129">Handle du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="02577-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="02577-130">*nPreviousProtocolOffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-131">Décalage du protocole précédent à partir du début du frame.</span><span class="sxs-lookup"><span data-stu-id="02577-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="02577-132">*lpInstData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02577-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02577-133">Pointeur vers les données d’instance fournies par le protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="02577-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="02577-134">La longueur des données d’instance ne peut pas être supérieure à celle \_ d’un PTR DWORD.</span><span class="sxs-lookup"><span data-stu-id="02577-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02577-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02577-135">Return value</span></span>

<span data-ttu-id="02577-136">Si la fonction réussit, la valeur de retour est un pointeur vers le premier octet après les données reconnues dans un frame ou **null** si les données reconnues sont la dernière partie des données d’un frame.</span><span class="sxs-lookup"><span data-stu-id="02577-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="02577-137">Si la fonction échoue, la valeur de retour est un pointeur vers les données reconnues.</span><span class="sxs-lookup"><span data-stu-id="02577-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="02577-138">Le paramètre *lpProtocol* passe le pointeur à la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="02577-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="02577-139">Notes</span><span class="sxs-lookup"><span data-stu-id="02577-139">Remarks</span></span>

<span data-ttu-id="02577-140">Moniteur réseau appelle la fonction **AttachProperties** pour chaque analyseur qui reconnaît un élément de données dans un frame.</span><span class="sxs-lookup"><span data-stu-id="02577-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="02577-141">Notez que l’analyseur détermine les propriétés qui existent dans les données reconnues, ainsi que l’emplacement de chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="02577-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="02577-142">Pendant l’implémentation de **AttachProperties**, appelez [AttachPropertyInstance](attachpropertyinstance.md) pour utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="02577-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="02577-143">Vous pouvez également appeler la fonction [AttachPropertyInstanceEx](attachpropertyinstanceex.md) pour modifier les données de propriété.</span><span class="sxs-lookup"><span data-stu-id="02577-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="02577-144">Toutefois, il est recommandé d’utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="02577-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="02577-145">Les fonctions **AttachPropertyInstanceEx** et **AttachPropertyInstance** sont appelées uniquement pour les propriétés qui existent dans les données reconnues.</span><span class="sxs-lookup"><span data-stu-id="02577-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="02577-146">Notez que Moniteur réseau a une [*base de données de propriétés*](p.md) pour l’analyseur qui contient une description de toutes les propriétés prises en charge par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="02577-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="02577-147">**Données d’instance**</span><span class="sxs-lookup"><span data-stu-id="02577-147">**Instance data**</span></span>

<span data-ttu-id="02577-148">Les données d’instance sont des informations transmises d’un analyseur à un autre.</span><span class="sxs-lookup"><span data-stu-id="02577-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="02577-149">Les données d’instance peuvent être des données qui sont inférieures ou égales à un \_ ptr DWORD en longueur, ou un pointeur vers des données, telles que des données de trame brutes, qui n’a pas besoin d’être alloué ou libéré par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="02577-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="02577-150">Dans le paramètre *lpInstData* des fonctions **AttachProperties** et [RecognizeFrame](recognizeframe.md) , moniteur réseau fournit un pointeur vers les données d’instance du protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="02577-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="02577-151">Vous pouvez définir les données d’instance de votre analyseur lors de l’implémentation de **RecognizeFrame**.</span><span class="sxs-lookup"><span data-stu-id="02577-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="02577-152">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="02577-152">For information on</span></span>                                          | <span data-ttu-id="02577-153">Consultez</span><span class="sxs-lookup"><span data-stu-id="02577-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="02577-154">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="02577-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="02577-155">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="02577-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="02577-156">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="02577-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="02577-157">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="02577-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="02577-158">Comment reconnaître des données.</span><span class="sxs-lookup"><span data-stu-id="02577-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="02577-159">Implémentation de RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="02577-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="02577-160">Comment créer une base de données de propriétés.</span><span class="sxs-lookup"><span data-stu-id="02577-160">How to create a property database.</span></span>                          | [<span data-ttu-id="02577-161">Implémentation du Registre</span><span class="sxs-lookup"><span data-stu-id="02577-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="02577-162">L’implémentation de **AttachProperties**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="02577-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="02577-163">Implémentation de AttachProperties</span><span class="sxs-lookup"><span data-stu-id="02577-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="02577-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02577-164">Requirements</span></span>



| <span data-ttu-id="02577-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02577-165">Requirement</span></span> | <span data-ttu-id="02577-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="02577-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02577-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02577-167">Minimum supported client</span></span><br/> | <span data-ttu-id="02577-168">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02577-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="02577-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02577-169">Minimum supported server</span></span><br/> | <span data-ttu-id="02577-170">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02577-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="02577-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="02577-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="02577-172"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="02577-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02577-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02577-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02577-174">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="02577-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="02577-175">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="02577-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="02577-176">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="02577-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




