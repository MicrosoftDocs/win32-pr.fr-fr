---
title: Type complexe LevelType
description: Définit une valeur de gravité qui détermine le niveau de détail des événements journalisés.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- LevelType type complexe EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102933"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="a66fa-104">Type complexe LevelType</span><span class="sxs-lookup"><span data-stu-id="a66fa-104">LevelType Complex Type</span></span>

<span data-ttu-id="a66fa-105">Définit une valeur de gravité qui détermine le niveau de détail des événements journalisés.</span><span class="sxs-lookup"><span data-stu-id="a66fa-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="a66fa-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="a66fa-106">Attributes</span></span>



| <span data-ttu-id="a66fa-107">Nom</span><span class="sxs-lookup"><span data-stu-id="a66fa-107">Name</span></span>    | <span data-ttu-id="a66fa-108">Type</span><span class="sxs-lookup"><span data-stu-id="a66fa-108">Type</span></span>                                                              | <span data-ttu-id="a66fa-109">Description</span><span class="sxs-lookup"><span data-stu-id="a66fa-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a66fa-110">message</span><span class="sxs-lookup"><span data-stu-id="a66fa-110">message</span></span> | [<span data-ttu-id="a66fa-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="a66fa-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a66fa-112">Nom complet localisé du niveau.</span><span class="sxs-lookup"><span data-stu-id="a66fa-112">The localized display name for the level.</span></span> <span data-ttu-id="a66fa-113">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="a66fa-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="a66fa-114">name</span><span class="sxs-lookup"><span data-stu-id="a66fa-114">name</span></span>    | <span data-ttu-id="a66fa-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="a66fa-115">**QName**</span></span>                                                         | <span data-ttu-id="a66fa-116">Nom à assigner à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="a66fa-116">The name to assign to this level.</span></span> <span data-ttu-id="a66fa-117">Ce nom doit être unique dans l’étendue du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a66fa-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="a66fa-118">symbole</span><span class="sxs-lookup"><span data-stu-id="a66fa-118">symbol</span></span>  | [<span data-ttu-id="a66fa-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="a66fa-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a66fa-120">Symbole à utiliser pour référencer le niveau dans votre application.</span><span class="sxs-lookup"><span data-stu-id="a66fa-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="a66fa-121">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le niveau dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="a66fa-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="a66fa-122">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="a66fa-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="a66fa-123">value</span><span class="sxs-lookup"><span data-stu-id="a66fa-123">value</span></span>   | [<span data-ttu-id="a66fa-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="a66fa-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="a66fa-125">Valeur de niveau.</span><span class="sxs-lookup"><span data-stu-id="a66fa-125">The level value.</span></span> <span data-ttu-id="a66fa-126">Vous pouvez spécifier des valeurs comprises dans la plage comprise entre 16 et 255.</span><span class="sxs-lookup"><span data-stu-id="a66fa-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="a66fa-127">Pour les valeurs de niveau prédéfinies, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a66fa-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="a66fa-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a66fa-128">Remarks</span></span>

<span data-ttu-id="a66fa-129">Voici les valeurs de niveau prédéfinies que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a66fa-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="a66fa-130">Ces valeurs sont définies dans le fichier Winmeta.xml inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a66fa-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="a66fa-131">Nom</span><span class="sxs-lookup"><span data-stu-id="a66fa-131">Name</span></span>              | <span data-ttu-id="a66fa-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a66fa-132">Value</span></span> | <span data-ttu-id="a66fa-133">Symbole</span><span class="sxs-lookup"><span data-stu-id="a66fa-133">Symbol</span></span>                    | <span data-ttu-id="a66fa-134">Description</span><span class="sxs-lookup"><span data-stu-id="a66fa-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a66fa-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="a66fa-135">win:Critical</span></span>      | <span data-ttu-id="a66fa-136">1</span><span class="sxs-lookup"><span data-stu-id="a66fa-136">1</span></span>     | <span data-ttu-id="a66fa-137">\_niveau WINEVENT \_ critique</span><span class="sxs-lookup"><span data-stu-id="a66fa-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="a66fa-138">Identifie un événement de sortie ou d’arrêt anormal.</span><span class="sxs-lookup"><span data-stu-id="a66fa-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="a66fa-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="a66fa-139">win:Error</span></span>         | <span data-ttu-id="a66fa-140">2</span><span class="sxs-lookup"><span data-stu-id="a66fa-140">2</span></span>     | <span data-ttu-id="a66fa-141">\_erreur de niveau WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="a66fa-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="a66fa-142">Identifie un événement d’erreur grave.</span><span class="sxs-lookup"><span data-stu-id="a66fa-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="a66fa-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="a66fa-143">win:Warning</span></span>       | <span data-ttu-id="a66fa-144">3</span><span class="sxs-lookup"><span data-stu-id="a66fa-144">3</span></span>     | <span data-ttu-id="a66fa-145">\_avertissement de niveau WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="a66fa-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="a66fa-146">Identifie un événement d’avertissement, tel qu’un échec d’allocation.</span><span class="sxs-lookup"><span data-stu-id="a66fa-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="a66fa-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="a66fa-147">win:Informational</span></span> | <span data-ttu-id="a66fa-148">4</span><span class="sxs-lookup"><span data-stu-id="a66fa-148">4</span></span>     | <span data-ttu-id="a66fa-149">\_informations de niveau WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="a66fa-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="a66fa-150">Identifie un événement qui n’est pas une erreur, tel qu’un événement d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="a66fa-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="a66fa-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="a66fa-151">win:Verbose</span></span>       | <span data-ttu-id="a66fa-152">5</span><span class="sxs-lookup"><span data-stu-id="a66fa-152">5</span></span>     | <span data-ttu-id="a66fa-153">WINEVENT \_ niveau de \_ détail</span><span class="sxs-lookup"><span data-stu-id="a66fa-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="a66fa-154">Identifie un événement de trace détaillé.</span><span class="sxs-lookup"><span data-stu-id="a66fa-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="a66fa-155">Des nombres plus élevés impliquent également des niveaux inférieurs.</span><span class="sxs-lookup"><span data-stu-id="a66fa-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="a66fa-156">Par exemple, si vous spécifiez Win : Warning, vous recevez tous les événements d’avertissement, d’erreur et critiques.</span><span class="sxs-lookup"><span data-stu-id="a66fa-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="a66fa-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a66fa-157">Requirements</span></span>



| <span data-ttu-id="a66fa-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a66fa-158">Requirement</span></span> | <span data-ttu-id="a66fa-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="a66fa-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a66fa-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a66fa-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a66fa-161">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a66fa-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a66fa-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a66fa-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a66fa-163">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a66fa-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





