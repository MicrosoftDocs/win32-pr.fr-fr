---
description: La fonction AttachPropertyInstance mappe une propriété existante à un emplacement spécifique dans les données reconnues.
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: AttachPropertyInstance, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 50ab07967605f8a24ba330a3cb13f80c833cf542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867030"
---
# <a name="attachpropertyinstance-function"></a><span data-ttu-id="81d97-103">AttachPropertyInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="81d97-103">AttachPropertyInstance function</span></span>

<span data-ttu-id="81d97-104">La fonction **AttachPropertyInstance** mappe une propriété existante à un emplacement spécifique dans les données reconnues.</span><span class="sxs-lookup"><span data-stu-id="81d97-104">The **AttachPropertyInstance** function maps an existing property to a specific location in the recognized data.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81d97-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="81d97-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81d97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d97-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-108">Handle vers le frame en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="81d97-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="81d97-109">Utilisez le descripteur passé à la DLL de l’analyseur dans le paramètre *hFrame* de la fonction [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="81d97-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="81d97-110">*hProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-111">Handle vers une structure [**PROPERTYINFO**](propertyinfo.md) qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="81d97-112">Lorsque vous implémentez la fonction d’exportation de [**Registre**](register-parser.md) , vous spécifiez la structure **PROPERTYINFO** qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="81d97-113">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-114">Longueur des données pour cette instance de la propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="81d97-115">*lpData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-116">Pointeur vers l’emplacement dans les données reconnues où se trouve la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="81d97-117">Utilisez le pointeur passé à la DLL de l’analyseur dans le paramètre *lpProtocol* de la fonction [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="81d97-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="81d97-118">*HelpID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-118">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-119">Identificateur (de 0 à 2047) utilisé pour définir l’aide contextuelle pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-119">Identifier (from 0 to 2047) used to set context-sensitive Help for the property.</span></span>

<span data-ttu-id="81d97-120">Le numéro d’identificateur est relatif au fichier d’aide associé à la [*base de données de propriétés de*](p.md)protocole.</span><span class="sxs-lookup"><span data-stu-id="81d97-120">The identifier number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="81d97-121">*IndentLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-121">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-122">Niveau de mise en retrait (de 0 à 15) utilisé pour afficher une propriété hiérarchiquement.</span><span class="sxs-lookup"><span data-stu-id="81d97-122">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="81d97-123">Moniteur réseau utilise les niveaux 0 à 14 pour mettre en retrait les propriétés.</span><span class="sxs-lookup"><span data-stu-id="81d97-123">Network Monitor uses levels 0 through 14 to indent properties.</span></span> <span data-ttu-id="81d97-124">Le niveau 15 est une valeur spéciale qui permet à un analyseur d’attacher une propriété masquée qui n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="81d97-124">Level 15 is a special value that allows a parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="81d97-125">*IFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81d97-125">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d97-126">Valeur de champ de bits qui indique l’ordre des BITs dans une propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-126">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="81d97-127">Les analyseurs précédents qui *définissent* le paramétrage de la valeur 0 ou 1 devraient *maintenant définir l'* erreur de l’IFLAG \_ .</span><span class="sxs-lookup"><span data-stu-id="81d97-127">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="81d97-128">Définissez ce paramètre sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="81d97-128">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="81d97-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="81d97-129">Value</span></span>                                                                                                                                                         | <span data-ttu-id="81d97-130">Signification</span><span class="sxs-lookup"><span data-stu-id="81d97-130">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="81d97-131"><dt>**\_erreur IFLAG**</dt></span><span class="sxs-lookup"><span data-stu-id="81d97-131"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="81d97-132">Les données du frame comportent une erreur.</span><span class="sxs-lookup"><span data-stu-id="81d97-132">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="81d97-133"><dt>**IFLAG \_ échangé**</dt></span><span class="sxs-lookup"><span data-stu-id="81d97-133"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="81d97-134">Au moment de l’attachement, le **mot** Byte n’est pas au format Intel.</span><span class="sxs-lookup"><span data-stu-id="81d97-134">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="81d97-135"><dt>**IFLAG \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="81d97-135"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="81d97-136">Au moment de l’attachement, la **chaîne** est Unicode.</span><span class="sxs-lookup"><span data-stu-id="81d97-136">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d97-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81d97-137">Return value</span></span>

<span data-ttu-id="81d97-138">Si la fonction réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="81d97-138">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="81d97-139">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="81d97-139">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d97-140">Notes</span><span class="sxs-lookup"><span data-stu-id="81d97-140">Remarks</span></span>

<span data-ttu-id="81d97-141">La fonction **AttachPropertyInstance** est appelée pendant l’implémentation de la fonction d’exportation [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="81d97-141">The **AttachPropertyInstance** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="81d97-142">Quand une propriété est attachée aux données, Moniteur réseau crée une structure [**PROPERTYINST**](propertyinst.md) qui définit l’instance de la propriété jointe.</span><span class="sxs-lookup"><span data-stu-id="81d97-142">When a property is attached to the data, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property.</span></span>

<span data-ttu-id="81d97-143">Pendant l’implémentation de [**AttachProperties**](attachproperties.md), appelez **AttachPropertyInstance** pour utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="81d97-143">During the implementation of [**AttachProperties**](attachproperties.md), call **AttachPropertyInstance** to use the data as it exists in the capture.</span></span> <span data-ttu-id="81d97-144">Vous pouvez également appeler la fonction [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) pour modifier les données de propriété.</span><span class="sxs-lookup"><span data-stu-id="81d97-144">You can also call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="81d97-145">Toutefois, il est recommandé d’utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="81d97-145">However, it is advised that you use the data as it exists in the capture.</span></span>



| <span data-ttu-id="81d97-146">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="81d97-146">For Information on</span></span>                                        | <span data-ttu-id="81d97-147">Consultez</span><span class="sxs-lookup"><span data-stu-id="81d97-147">See</span></span>                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="81d97-148">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="81d97-148">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="81d97-149">**Analyseurs**</span><span class="sxs-lookup"><span data-stu-id="81d97-149">**Parsers**</span></span>](parsers.md)                                         |
| <span data-ttu-id="81d97-150">Comment appeler **AttachPropertyInstance**.</span><span class="sxs-lookup"><span data-stu-id="81d97-150">How to call **AttachPropertyInstance**.</span></span>                   | [<span data-ttu-id="81d97-151">Implémentation de AttachProperties</span><span class="sxs-lookup"><span data-stu-id="81d97-151">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="81d97-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81d97-152">Requirements</span></span>



| <span data-ttu-id="81d97-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81d97-153">Requirement</span></span> | <span data-ttu-id="81d97-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="81d97-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81d97-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81d97-155">Minimum supported client</span></span><br/> | <span data-ttu-id="81d97-156">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81d97-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="81d97-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81d97-157">Minimum supported server</span></span><br/> | <span data-ttu-id="81d97-158">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81d97-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81d97-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="81d97-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d97-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d97-160"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="81d97-161">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81d97-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="81d97-162"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81d97-162"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="81d97-163">DLL</span><span class="sxs-lookup"><span data-stu-id="81d97-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d97-164"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81d97-164"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d97-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81d97-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d97-166">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="81d97-166">**AttachProperties**</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="81d97-167">**AttachPropertyInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="81d97-167">**AttachPropertyInstanceEx**</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="81d97-168">**PROPERTYINST**</span><span class="sxs-lookup"><span data-stu-id="81d97-168">**PROPERTYINST**</span></span>](propertyinst.md)
</dt> </dl>

 

 




