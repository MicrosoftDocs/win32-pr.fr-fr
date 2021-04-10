---
title: Type complexe OpcodeType
description: Définit une opération dans un composant de l’application.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- OpcodeType type complexe EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106024"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="92c4f-104">Type complexe OpcodeType</span><span class="sxs-lookup"><span data-stu-id="92c4f-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="92c4f-105">Définit une opération dans un composant de l’application.</span><span class="sxs-lookup"><span data-stu-id="92c4f-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="92c4f-106">Utilisé conjointement à une tâche pour identifier la section de l’application qui enregistre l’événement.</span><span class="sxs-lookup"><span data-stu-id="92c4f-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
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
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="92c4f-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="92c4f-107">Attributes</span></span>



| <span data-ttu-id="92c4f-108">Nom</span><span class="sxs-lookup"><span data-stu-id="92c4f-108">Name</span></span>     | <span data-ttu-id="92c4f-109">Type</span><span class="sxs-lookup"><span data-stu-id="92c4f-109">Type</span></span>                                                              | <span data-ttu-id="92c4f-110">Description</span><span class="sxs-lookup"><span data-stu-id="92c4f-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c4f-111">message</span><span class="sxs-lookup"><span data-stu-id="92c4f-111">message</span></span>  | [<span data-ttu-id="92c4f-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="92c4f-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="92c4f-113">Nom complet localisé pour l’opcode.</span><span class="sxs-lookup"><span data-stu-id="92c4f-113">The localized display name for the opcode.</span></span> <span data-ttu-id="92c4f-114">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="92c4f-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="92c4f-115">mofValue</span><span class="sxs-lookup"><span data-stu-id="92c4f-115">mofValue</span></span> | [<span data-ttu-id="92c4f-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="92c4f-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="92c4f-117">Réservé à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="92c4f-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="92c4f-118">name</span><span class="sxs-lookup"><span data-stu-id="92c4f-118">name</span></span>     | <span data-ttu-id="92c4f-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="92c4f-119">**QName**</span></span>                                                         | <span data-ttu-id="92c4f-120">Nom de l’opcode.</span><span class="sxs-lookup"><span data-stu-id="92c4f-120">The name of the opcode.</span></span> <span data-ttu-id="92c4f-121">Ce nom doit être unique dans l’étendue de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="92c4f-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="92c4f-122">symbole</span><span class="sxs-lookup"><span data-stu-id="92c4f-122">symbol</span></span>   | [<span data-ttu-id="92c4f-123">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="92c4f-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="92c4f-124">Symbole à utiliser pour référencer l’opcode dans votre application.</span><span class="sxs-lookup"><span data-stu-id="92c4f-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="92c4f-125">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour l’opcode dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="92c4f-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="92c4f-126">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="92c4f-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="92c4f-127">value</span><span class="sxs-lookup"><span data-stu-id="92c4f-127">value</span></span>    | [<span data-ttu-id="92c4f-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="92c4f-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="92c4f-129">Valeur de l’opcode.</span><span class="sxs-lookup"><span data-stu-id="92c4f-129">The opcode value.</span></span> <span data-ttu-id="92c4f-130">Vous pouvez spécifier des valeurs dans la plage 10 et 239.</span><span class="sxs-lookup"><span data-stu-id="92c4f-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="92c4f-131">Pour obtenir la liste des valeurs opcode prédéfinies, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="92c4f-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="92c4f-132">Notes</span><span class="sxs-lookup"><span data-stu-id="92c4f-132">Remarks</span></span>

<span data-ttu-id="92c4f-133">Voici les valeurs opcode prédéfinies que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="92c4f-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="92c4f-134">Ces valeurs sont définies dans le fichier Winmeta.xml inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="92c4f-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="92c4f-135">Nom</span><span class="sxs-lookup"><span data-stu-id="92c4f-135">Name</span></span>          | <span data-ttu-id="92c4f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="92c4f-136">Value</span></span> | <span data-ttu-id="92c4f-137">Symbole</span><span class="sxs-lookup"><span data-stu-id="92c4f-137">Symbol</span></span>                      | <span data-ttu-id="92c4f-138">Description</span><span class="sxs-lookup"><span data-stu-id="92c4f-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c4f-139">Win : info</span><span class="sxs-lookup"><span data-stu-id="92c4f-139">win:Info</span></span>      | <span data-ttu-id="92c4f-140">0</span><span class="sxs-lookup"><span data-stu-id="92c4f-140">0</span></span>     | <span data-ttu-id="92c4f-141">\_informations sur l’OPCODE WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="92c4f-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="92c4f-142">Événement d'informations.</span><span class="sxs-lookup"><span data-stu-id="92c4f-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="92c4f-143">Win : Démarrer</span><span class="sxs-lookup"><span data-stu-id="92c4f-143">win:Start</span></span>     | <span data-ttu-id="92c4f-144">1</span><span class="sxs-lookup"><span data-stu-id="92c4f-144">1</span></span>     | <span data-ttu-id="92c4f-145">début de l' \_ OPCODE WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="92c4f-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="92c4f-146">Événement qui représente le démarrage d’une activité.</span><span class="sxs-lookup"><span data-stu-id="92c4f-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="92c4f-147">Win : arrêter</span><span class="sxs-lookup"><span data-stu-id="92c4f-147">win:Stop</span></span>      | <span data-ttu-id="92c4f-148">2</span><span class="sxs-lookup"><span data-stu-id="92c4f-148">2</span></span>     | <span data-ttu-id="92c4f-149">arrêt de l' \_ OPCODE WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="92c4f-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="92c4f-150">Événement qui représente l’arrêt d’une activité.</span><span class="sxs-lookup"><span data-stu-id="92c4f-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="92c4f-151">L’événement correspond au dernier événement de début non couplé.</span><span class="sxs-lookup"><span data-stu-id="92c4f-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="92c4f-152">Win : DC \_ Start</span><span class="sxs-lookup"><span data-stu-id="92c4f-152">win:DC\_Start</span></span> | <span data-ttu-id="92c4f-153">3</span><span class="sxs-lookup"><span data-stu-id="92c4f-153">3</span></span>     | <span data-ttu-id="92c4f-154">WINEVENT \_ OPCODE \_ DC \_ Start</span><span class="sxs-lookup"><span data-stu-id="92c4f-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="92c4f-155">Événement qui représente le démarrage de la collecte de données.</span><span class="sxs-lookup"><span data-stu-id="92c4f-155">An event that represents data collection starting.</span></span> <span data-ttu-id="92c4f-156">Il s’agit des types d’événements d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="92c4f-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="92c4f-157">Win : \_ arrêt DC</span><span class="sxs-lookup"><span data-stu-id="92c4f-157">win:DC\_Stop</span></span>  | <span data-ttu-id="92c4f-158">4</span><span class="sxs-lookup"><span data-stu-id="92c4f-158">4</span></span>     | <span data-ttu-id="92c4f-159">WINEVENT \_ OPCODE \_ DC \_ Stop</span><span class="sxs-lookup"><span data-stu-id="92c4f-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="92c4f-160">Événement qui représente l’arrêt de la collecte de données.</span><span class="sxs-lookup"><span data-stu-id="92c4f-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="92c4f-161">Il s’agit des types d’événements d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="92c4f-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="92c4f-162">Win : extension</span><span class="sxs-lookup"><span data-stu-id="92c4f-162">win:Extension</span></span> | <span data-ttu-id="92c4f-163">5</span><span class="sxs-lookup"><span data-stu-id="92c4f-163">5</span></span>     | <span data-ttu-id="92c4f-164">\_extension OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="92c4f-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="92c4f-165">Evénement d'extension.</span><span class="sxs-lookup"><span data-stu-id="92c4f-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="92c4f-166">Win : répondre</span><span class="sxs-lookup"><span data-stu-id="92c4f-166">win:Reply</span></span>     | <span data-ttu-id="92c4f-167">6</span><span class="sxs-lookup"><span data-stu-id="92c4f-167">6</span></span>     | <span data-ttu-id="92c4f-168">\_réponse OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="92c4f-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="92c4f-169">Événement de réponse.</span><span class="sxs-lookup"><span data-stu-id="92c4f-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="92c4f-170">Win : reprendre</span><span class="sxs-lookup"><span data-stu-id="92c4f-170">win:Resume</span></span>    | <span data-ttu-id="92c4f-171">7</span><span class="sxs-lookup"><span data-stu-id="92c4f-171">7</span></span>     | <span data-ttu-id="92c4f-172">WINEVENT \_ OPCODE \_ Resume</span><span class="sxs-lookup"><span data-stu-id="92c4f-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="92c4f-173">Événement qui représente une activité qui reprend après avoir été suspendue.</span><span class="sxs-lookup"><span data-stu-id="92c4f-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="92c4f-174">Win : suspendre</span><span class="sxs-lookup"><span data-stu-id="92c4f-174">win:Suspend</span></span>   | <span data-ttu-id="92c4f-175">8</span><span class="sxs-lookup"><span data-stu-id="92c4f-175">8</span></span>     | <span data-ttu-id="92c4f-176">WINEVENT \_ OPCODE \_ suspend</span><span class="sxs-lookup"><span data-stu-id="92c4f-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="92c4f-177">Événement qui représente l’activité en cours de suspension en attente de la fin d’une autre activité.</span><span class="sxs-lookup"><span data-stu-id="92c4f-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="92c4f-178">Win : envoyer</span><span class="sxs-lookup"><span data-stu-id="92c4f-178">win:Send</span></span>      | <span data-ttu-id="92c4f-179">9</span><span class="sxs-lookup"><span data-stu-id="92c4f-179">9</span></span>     | <span data-ttu-id="92c4f-180">WINEVENT \_ OPCODE \_ Send</span><span class="sxs-lookup"><span data-stu-id="92c4f-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="92c4f-181">Événement qui représente le transfert de l’activité vers un autre composant.</span><span class="sxs-lookup"><span data-stu-id="92c4f-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="92c4f-182">Win : recevoir</span><span class="sxs-lookup"><span data-stu-id="92c4f-182">win:Receive</span></span>   | <span data-ttu-id="92c4f-183">240</span><span class="sxs-lookup"><span data-stu-id="92c4f-183">240</span></span>   | <span data-ttu-id="92c4f-184">réception de l' \_ OPCODE WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="92c4f-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="92c4f-185">Événement qui représente la réception d’un transfert d’activité à partir d’un autre composant.</span><span class="sxs-lookup"><span data-stu-id="92c4f-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="92c4f-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92c4f-186">Requirements</span></span>



| <span data-ttu-id="92c4f-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92c4f-187">Requirement</span></span> | <span data-ttu-id="92c4f-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="92c4f-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92c4f-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92c4f-189">Minimum supported client</span></span><br/> | <span data-ttu-id="92c4f-190">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92c4f-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92c4f-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92c4f-191">Minimum supported server</span></span><br/> | <span data-ttu-id="92c4f-192">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92c4f-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





