---
title: Type complexe StructDefinitionType
description: Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement. | Type complexe StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525831"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="bd204-105">Type complexe StructDefinitionType</span><span class="sxs-lookup"><span data-stu-id="bd204-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="bd204-106">Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="bd204-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bd204-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bd204-107">Child elements</span></span>



| <span data-ttu-id="bd204-108">Élément</span><span class="sxs-lookup"><span data-stu-id="bd204-108">Element</span></span>                                                               | <span data-ttu-id="bd204-109">Type</span><span class="sxs-lookup"><span data-stu-id="bd204-109">Type</span></span>                                                                             | <span data-ttu-id="bd204-110">Description</span><span class="sxs-lookup"><span data-stu-id="bd204-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="bd204-111">**data**</span><span class="sxs-lookup"><span data-stu-id="bd204-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="bd204-112">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="bd204-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="bd204-113">Définit un élément de données que vous souhaitez inclure dans la structure.</span><span class="sxs-lookup"><span data-stu-id="bd204-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="bd204-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="bd204-114">Attributes</span></span>



| <span data-ttu-id="bd204-115">Nom</span><span class="sxs-lookup"><span data-stu-id="bd204-115">Name</span></span>   | <span data-ttu-id="bd204-116">Type</span><span class="sxs-lookup"><span data-stu-id="bd204-116">Type</span></span>                                                            | <span data-ttu-id="bd204-117">Description</span><span class="sxs-lookup"><span data-stu-id="bd204-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd204-118">count</span><span class="sxs-lookup"><span data-stu-id="bd204-118">count</span></span>  | [<span data-ttu-id="bd204-119">**CountType**</span><span class="sxs-lookup"><span data-stu-id="bd204-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="bd204-120">Nombre d’éléments dans un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="bd204-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="bd204-121">Cet attribut indique que la structure définit un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="bd204-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="bd204-122">Vous pouvez spécifier le nombre réel ou le nom d’un élément de données en dehors de la structure qui contient le nombre.</span><span class="sxs-lookup"><span data-stu-id="bd204-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="bd204-123">length</span><span class="sxs-lookup"><span data-stu-id="bd204-123">length</span></span> | [<span data-ttu-id="bd204-124">**LengthType**</span><span class="sxs-lookup"><span data-stu-id="bd204-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="bd204-125">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="bd204-125">Not available.</span></span><br/> <span data-ttu-id="bd204-126">**Windows Server 2008 et Windows Vista :** Longueur de cette structure, en octets.</span><span class="sxs-lookup"><span data-stu-id="bd204-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="bd204-127">Non disponible à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bd204-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="bd204-128">name</span><span class="sxs-lookup"><span data-stu-id="bd204-128">name</span></span>   | <span data-ttu-id="bd204-129">string</span><span class="sxs-lookup"><span data-stu-id="bd204-129">string</span></span>                                                          | <span data-ttu-id="bd204-130">Nom de la structure.</span><span class="sxs-lookup"><span data-stu-id="bd204-130">The name to the structure.</span></span> <span data-ttu-id="bd204-131">Vous pouvez utiliser le nom pour faire référence à l’élément de données dans votre fragment XML si vous spécifiez une section [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="bd204-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="bd204-132">**Windows Vista :** Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bd204-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bd204-133">Notes</span><span class="sxs-lookup"><span data-stu-id="bd204-133">Remarks</span></span>

<span data-ttu-id="bd204-134">Les fournisseurs écrivent la structure en tant qu’objet BLOB et non en tant que membres individuels de la structure.</span><span class="sxs-lookup"><span data-stu-id="bd204-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="bd204-135">Si la structure C que vous écrivez contient des pointeurs (par exemple, un pointeur de type LPWSTR), les données d’événement contiendront la valeur du pointeur, et non les données déréférencées.</span><span class="sxs-lookup"><span data-stu-id="bd204-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="bd204-136">Vous ne devez pas utiliser des structures mais devez plutôt définir des éléments de données pour chaque membre et les écrire séparément.</span><span class="sxs-lookup"><span data-stu-id="bd204-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="bd204-137">Si vous décidez d’utiliser la structure, la structure doit contenir uniquement des types intégraux et vous devez vous assurer que les membres de la structure sont alignés sur une limite de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="bd204-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="bd204-138">Si vous ne le faites pas, vous risquez de recevoir des erreurs d’alignement quand vous tentez d’accéder aux données.</span><span class="sxs-lookup"><span data-stu-id="bd204-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="bd204-139">Envisagez \# d’utiliser la directive pragma Pack () pour forcer l’alignement sur une limite de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="bd204-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd204-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd204-140">Requirements</span></span>



| <span data-ttu-id="bd204-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd204-141">Requirement</span></span> | <span data-ttu-id="bd204-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd204-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bd204-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd204-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bd204-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd204-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bd204-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd204-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bd204-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd204-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





