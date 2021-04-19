---
description: La fonction AttachPropertyInstanceEx mappe une propriété existante à un emplacement spécifique dans les données reconnues et modifie la valeur des données de propriété.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: AttachPropertyInstanceEx, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544834"
---
# <a name="attachpropertyinstanceex-function"></a><span data-ttu-id="dd81c-103">AttachPropertyInstanceEx fonction)</span><span class="sxs-lookup"><span data-stu-id="dd81c-103">AttachPropertyInstanceEx function</span></span>

<span data-ttu-id="dd81c-104">La fonction **AttachPropertyInstanceEx** mappe une propriété existante à un emplacement spécifique dans les données reconnues et modifie la valeur des données de propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-104">The **AttachPropertyInstanceEx** function maps an existing property to a specific location in the recognized data, and modifies the value of the property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd81c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd81c-105">Syntax</span></span>


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dd81c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd81c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd81c-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-108">Handle vers le frame en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="dd81c-108">Handle to the frame that is being parsed.</span></span> <span data-ttu-id="dd81c-109">Utilisez le descripteur passé à la DLL de l’analyseur dans le paramètre *hFrame* de la fonction [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="dd81c-109">Use the handle passed to the parser DLL in the *hFrame* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-110">*hProperty* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-111">Handle vers une structure [**PROPERTYINFO**](propertyinfo.md) qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-111">Handle to a [**PROPERTYINFO**](propertyinfo.md) structure that defines the property.</span></span> <span data-ttu-id="dd81c-112">Lorsque vous implémentez la fonction d’exportation de [**Registre**](register-parser.md) , vous spécifiez la structure **PROPERTYINFO** qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-112">When you implement the [**Register**](register-parser.md) export function you specify the **PROPERTYINFO** structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-113">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-113">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-114">Longueur des données pour cette instance de la propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-114">Length of the data for this instance of the property.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-115">*lpData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-115">*lpData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-116">Pointeur vers l’emplacement dans les données reconnues où se trouve la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-116">Pointer to the location in the recognized data where the property value is located.</span></span> <span data-ttu-id="dd81c-117">Utilisez le pointeur passé à la DLL de l’analyseur dans le paramètre *lpProtocol* de la fonction [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="dd81c-117">Use the pointer passed to the parser DLL in the *lpProtocol* parameter of the [**AttachProperties**](attachproperties.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-118">*LengthEx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-118">*LengthEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-119">Longueur de la longueur des données étendues, en octets.</span><span class="sxs-lookup"><span data-stu-id="dd81c-119">Length of the extended data   length in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-120">*lpDataEx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-120">*lpDataEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-121">Pointeur vers les données étendues, qui est généralement une variable de pile qui contient les données d’extension.</span><span class="sxs-lookup"><span data-stu-id="dd81c-121">Pointer to the extended data, which is typically a stack variable that contains the extend data.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-122">*HelpID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-122">*HelpID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-123">Identificateur (de 0 à 2047) utilisé pour définir une aide contextuelle pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-123">Identifier (from 0 to 2047) used to set context-sensitive Help for a property.</span></span>

<span data-ttu-id="dd81c-124">Le numéro *HelpID* est relatif au fichier d’aide associé à la [*base de données de propriétés de*](p.md)protocole.</span><span class="sxs-lookup"><span data-stu-id="dd81c-124">The *HelpID* number is relative to the Help file associated with the protocol [*property database*](p.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-125">*IndentLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-125">*IndentLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-126">Niveau de mise en retrait (de 0 à 15) utilisé pour afficher une propriété hiérarchiquement.</span><span class="sxs-lookup"><span data-stu-id="dd81c-126">Indentation level (from 0 to 15) used to display a property hierarchically.</span></span>

<span data-ttu-id="dd81c-127">Moniteur réseau utilise les niveaux 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="dd81c-127">Network Monitor uses levels 0 through 9.</span></span> <span data-ttu-id="dd81c-128">Le niveau 15 est une valeur spéciale qui permet à l’analyseur d’attacher une propriété masquée qui n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="dd81c-128">Level 15 is a special value that allows the parser to attach a hidden property that is not visible.</span></span>

</dd> <dt>

<span data-ttu-id="dd81c-129">*IFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-129">*IFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd81c-130">Valeur de champ de bits qui indique l’ordre des BITs dans une propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-130">A BIT field value that indicates the order of the BITs within a property.</span></span> <span data-ttu-id="dd81c-131">Les analyseurs précédents qui *définissent* le paramétrage de la valeur 0 ou 1 devraient *maintenant définir l'* erreur de l’IFLAG \_ .</span><span class="sxs-lookup"><span data-stu-id="dd81c-131">Previous parsers that set *fError* to 0 or 1, should now set *fError* to IFLAG\_ERROR.</span></span> <span data-ttu-id="dd81c-132">Définissez ce paramètre sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd81c-132">Set this parameter to one of the following values.</span></span>



| <span data-ttu-id="dd81c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd81c-133">Value</span></span>                                                                                                                                                         | <span data-ttu-id="dd81c-134">Signification</span><span class="sxs-lookup"><span data-stu-id="dd81c-134">Meaning</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <span data-ttu-id="dd81c-135"><dt>**\_erreur IFLAG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd81c-135"><dt>**IFLAG\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="dd81c-136">Les données du frame comportent une erreur.</span><span class="sxs-lookup"><span data-stu-id="dd81c-136">Data in the frame has an error.</span></span><br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <span data-ttu-id="dd81c-137"><dt>**IFLAG \_ échangé**</dt></span><span class="sxs-lookup"><span data-stu-id="dd81c-137"><dt>**IFLAG\_SWAPPED**</dt></span></span> </dl> | <span data-ttu-id="dd81c-138">Au moment de l’attachement, le **mot** Byte n’est pas au format Intel.</span><span class="sxs-lookup"><span data-stu-id="dd81c-138">At attach time, **WORD** byte is a non-Intel format.</span></span><br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <span data-ttu-id="dd81c-139"><dt>**IFLAG \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="dd81c-139"><dt>**IFLAG\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="dd81c-140">Au moment de l’attachement, la **chaîne** est Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd81c-140">At attach time, **STRING** is Unicode.</span></span><br/>               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd81c-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd81c-141">Return value</span></span>

<span data-ttu-id="dd81c-142">Si la fonction réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="dd81c-142">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="dd81c-143">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="dd81c-143">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd81c-144">Notes</span><span class="sxs-lookup"><span data-stu-id="dd81c-144">Remarks</span></span>

<span data-ttu-id="dd81c-145">La fonction **AttachPropertyInstanceEx** est appelée pendant l’implémentation de la fonction d’exportation [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="dd81c-145">The **AttachPropertyInstanceEx** function is called during the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span> <span data-ttu-id="dd81c-146">Quand une propriété est attachée aux données à l’aide de AttachPropertyInstanceEx, Moniteur réseau crée une structure [**PROPERTYINST**](propertyinst.md) qui définit l’instance de la propriété jointe et une structure [**PROPERTYINSTEX**](propertyinstex.md) qui définit les données étendues.</span><span class="sxs-lookup"><span data-stu-id="dd81c-146">When a property is attached to the data using AttachPropertyInstanceEx, Network Monitor creates a [**PROPERTYINST**](propertyinst.md) structure that defines the instance of the attached property and a [**PROPERTYINSTEX**](propertyinstex.md) structure that defines the extended data.</span></span>

<span data-ttu-id="dd81c-147">Si **AttachPropertyInstanceEx** est appelée et qu’aucune donnée étendue n’est fournie, le paramètre *lpDataEx* est **null** ou le paramètre *LengthEx* est 0, l’appel **AttachPropertyInstanceEx** est fonctionnellement équivalent à un appel [**AttachPropertyInstance**](attachpropertyinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="dd81c-147">If **AttachPropertyInstanceEx** is called and no extended data is provided, the *lpDataEx* parameter is **NULL** or the *LengthEx* parameter is 0, the **AttachPropertyInstanceEx** call is functionally equivalent to an [**AttachPropertyInstance**](attachpropertyinstance.md) call.</span></span>

<span data-ttu-id="dd81c-148">Pendant l’implémentation de [**AttachProperties**](attachproperties.md), appelez [**AttachPropertyInstance**](attachpropertyinstance.md) pour utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="dd81c-148">During the implementation of [**AttachProperties**](attachproperties.md), call [**AttachPropertyInstance**](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="dd81c-149">Vous pouvez également appeler la fonction **AttachPropertyInstanceEx** pour modifier les données de propriété.</span><span class="sxs-lookup"><span data-stu-id="dd81c-149">You can also call **AttachPropertyInstanceEx** function to modify the property data.</span></span> <span data-ttu-id="dd81c-150">Toutefois, il est recommandé d’utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="dd81c-150">However, it is advised that you use the data as it exists in the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd81c-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd81c-151">Requirements</span></span>



| <span data-ttu-id="dd81c-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd81c-152">Requirement</span></span> | <span data-ttu-id="dd81c-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd81c-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd81c-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd81c-154">Minimum supported client</span></span><br/> | <span data-ttu-id="dd81c-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dd81c-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd81c-156">Minimum supported server</span></span><br/> | <span data-ttu-id="dd81c-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd81c-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd81c-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd81c-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd81c-159"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd81c-159"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="dd81c-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd81c-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd81c-161"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd81c-161"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd81c-162">DLL</span><span class="sxs-lookup"><span data-stu-id="dd81c-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd81c-163"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd81c-163"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




