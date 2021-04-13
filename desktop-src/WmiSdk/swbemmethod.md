---
description: Vous pouvez utiliser les propriétés de l’objet SWbemMethod pour inspecter une définition de méthode unique d’un objet WMI. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objet SWbemMethod (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528486"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="301a6-104">Objet SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="301a6-104">SWbemMethod object</span></span>

<span data-ttu-id="301a6-105">Vous pouvez utiliser les propriétés de l’objet **SWbemMethod** pour inspecter une définition de méthode unique d’un objet WMI.</span><span class="sxs-lookup"><span data-stu-id="301a6-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="301a6-106">Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="301a6-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="301a6-107">Cet objet peut être utilisé pour inspecter les définitions des méthodes.</span><span class="sxs-lookup"><span data-stu-id="301a6-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="301a6-108">Pour appeler les méthodes, vous devez utiliser l’accès direct (consultez [manipulation d’informations sur la classe et](manipulating-class-and-instance-information.md)SWbemServices.Exel’instance) sur un objet [**SWbemObject**](swbemobject.md) (mécanisme recommandé) ou l’appel [**cMethod**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="301a6-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="301a6-109">Dans cette version de l’API, l’accès en écriture aux informations de méthode n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="301a6-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="301a6-110">Si vous souhaitez définir des méthodes ou modifier des définitions de méthode existantes, vous pouvez définir les modifications de méthode dans un fichier MOF et soumettre les modifications à l’aide du [compilateur MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="301a6-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="301a6-111">Vous pouvez également utiliser l' [API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="301a6-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="301a6-112">Membres</span><span class="sxs-lookup"><span data-stu-id="301a6-112">Members</span></span>

<span data-ttu-id="301a6-113">L’objet **SWbemMethod** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="301a6-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="301a6-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="301a6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="301a6-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="301a6-115">Properties</span></span>

<span data-ttu-id="301a6-116">L’objet **SWbemMethod** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="301a6-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="301a6-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="301a6-117">Property</span></span>                                                      | <span data-ttu-id="301a6-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="301a6-118">Access type</span></span>          | <span data-ttu-id="301a6-119">Description</span><span class="sxs-lookup"><span data-stu-id="301a6-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="301a6-120">**Inparamètres**</span><span class="sxs-lookup"><span data-stu-id="301a6-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="301a6-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="301a6-121">Read-only</span></span><br/> | <span data-ttu-id="301a6-122">Objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres d’entrée pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="301a6-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="301a6-123">**Nom**</span><span class="sxs-lookup"><span data-stu-id="301a6-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="301a6-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="301a6-124">Read-only</span></span><br/> | <span data-ttu-id="301a6-125">Nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="301a6-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="301a6-126">**Origine**</span><span class="sxs-lookup"><span data-stu-id="301a6-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="301a6-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="301a6-127">Read-only</span></span><br/> | <span data-ttu-id="301a6-128">Classe d’origine de la méthode.</span><span class="sxs-lookup"><span data-stu-id="301a6-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="301a6-129">**Paramètres de paramètres**</span><span class="sxs-lookup"><span data-stu-id="301a6-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="301a6-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="301a6-130">Read-only</span></span><br/> | <span data-ttu-id="301a6-131">Objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres de sortie et le type de retour de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="301a6-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="301a6-132">**Qualificateurs\_**</span><span class="sxs-lookup"><span data-stu-id="301a6-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="301a6-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="301a6-133">Read-only</span></span><br/> | <span data-ttu-id="301a6-134">Objet [**SWbemQualifierSet**](swbemqualifierset.md) qui contient les qualificateurs de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="301a6-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="301a6-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="301a6-135">Requirements</span></span>



| <span data-ttu-id="301a6-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="301a6-136">Requirement</span></span> | <span data-ttu-id="301a6-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="301a6-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="301a6-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="301a6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="301a6-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="301a6-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="301a6-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="301a6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="301a6-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="301a6-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="301a6-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="301a6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="301a6-143"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="301a6-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="301a6-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="301a6-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="301a6-145"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="301a6-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="301a6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="301a6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="301a6-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="301a6-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="301a6-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="301a6-148">CLSID</span></span><br/>                    | <span data-ttu-id="301a6-149">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="301a6-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="301a6-150">IID</span><span class="sxs-lookup"><span data-stu-id="301a6-150">IID</span></span><br/>                      | <span data-ttu-id="301a6-151">IID \_ ISWbemMethod</span><span class="sxs-lookup"><span data-stu-id="301a6-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="301a6-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="301a6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301a6-153">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="301a6-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




