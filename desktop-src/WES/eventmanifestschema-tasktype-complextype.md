---
title: Type complexe TaskType
description: Définit un composant ou un sous-composant d’une application. | Type complexe TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType type complexe EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535782"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="19d82-105">Type complexe TaskType</span><span class="sxs-lookup"><span data-stu-id="19d82-105">TaskType Complex Type</span></span>

<span data-ttu-id="19d82-106">Définit un composant ou un sous-composant d’une application.</span><span class="sxs-lookup"><span data-stu-id="19d82-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
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
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="19d82-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="19d82-107">Child elements</span></span>



| <span data-ttu-id="19d82-108">Élément</span><span class="sxs-lookup"><span data-stu-id="19d82-108">Element</span></span>                                                         | <span data-ttu-id="19d82-109">Type</span><span class="sxs-lookup"><span data-stu-id="19d82-109">Type</span></span>                                                                     | <span data-ttu-id="19d82-110">Description</span><span class="sxs-lookup"><span data-stu-id="19d82-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19d82-111">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="19d82-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="19d82-112">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="19d82-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="19d82-113">Définit une liste d’OpCodes spécifiques à une tâche.</span><span class="sxs-lookup"><span data-stu-id="19d82-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="19d82-114">Vous ne pouvez pas utiliser les valeurs opcode définies dans Winmeta.xml pour les OpCodes spécifiques à la tâche.</span><span class="sxs-lookup"><span data-stu-id="19d82-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="19d82-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="19d82-115">Attributes</span></span>



| <span data-ttu-id="19d82-116">Nom</span><span class="sxs-lookup"><span data-stu-id="19d82-116">Name</span></span>      | <span data-ttu-id="19d82-117">Type</span><span class="sxs-lookup"><span data-stu-id="19d82-117">Type</span></span>                                                              | <span data-ttu-id="19d82-118">Description</span><span class="sxs-lookup"><span data-stu-id="19d82-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19d82-119">eventGUID</span><span class="sxs-lookup"><span data-stu-id="19d82-119">eventGUID</span></span> | [<span data-ttu-id="19d82-120">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="19d82-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="19d82-121">Identificateur global unique, au format de Registre, qui identifie la tâche.</span><span class="sxs-lookup"><span data-stu-id="19d82-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="19d82-122">Cet attribut est requis si vous utilisez l’argument-MOF message compiler pour générer une classe MOF pour la prise en charge de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="19d82-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="19d82-123">message</span><span class="sxs-lookup"><span data-stu-id="19d82-123">message</span></span>   | [<span data-ttu-id="19d82-124">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="19d82-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="19d82-125">Nom complet localisé de la tâche.</span><span class="sxs-lookup"><span data-stu-id="19d82-125">The localized display name for the task.</span></span> <span data-ttu-id="19d82-126">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="19d82-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="19d82-127">name</span><span class="sxs-lookup"><span data-stu-id="19d82-127">name</span></span>      | <span data-ttu-id="19d82-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="19d82-128">**QName**</span></span>                                                         | <span data-ttu-id="19d82-129">Nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="19d82-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="19d82-130">symbole</span><span class="sxs-lookup"><span data-stu-id="19d82-130">symbol</span></span>    | [<span data-ttu-id="19d82-131">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="19d82-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="19d82-132">Symbole à utiliser pour référencer la tâche dans votre application.</span><span class="sxs-lookup"><span data-stu-id="19d82-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="19d82-133">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour la tâche dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="19d82-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="19d82-134">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="19d82-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="19d82-135">value</span><span class="sxs-lookup"><span data-stu-id="19d82-135">value</span></span>     | [<span data-ttu-id="19d82-136">**UInt16Type**</span><span class="sxs-lookup"><span data-stu-id="19d82-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="19d82-137">Valeur numérique qui identifie de façon unique cette tâche dans la liste des tâches que le fournisseur définit.</span><span class="sxs-lookup"><span data-stu-id="19d82-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="19d82-138">La valeur doit être comprise entre 1 et 239.</span><span class="sxs-lookup"><span data-stu-id="19d82-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="19d82-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="19d82-139">Examples</span></span>

<span data-ttu-id="19d82-140">L’exemple suivant montre comment spécifier une tâche.</span><span class="sxs-lookup"><span data-stu-id="19d82-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="19d82-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19d82-141">Requirements</span></span>



| <span data-ttu-id="19d82-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19d82-142">Requirement</span></span> | <span data-ttu-id="19d82-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="19d82-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19d82-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19d82-144">Minimum supported client</span></span><br/> | <span data-ttu-id="19d82-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19d82-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19d82-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19d82-146">Minimum supported server</span></span><br/> | <span data-ttu-id="19d82-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19d82-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





