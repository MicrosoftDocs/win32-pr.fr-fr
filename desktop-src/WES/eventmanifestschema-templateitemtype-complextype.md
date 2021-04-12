---
title: Type complexe TemplateItemType
description: Modèle qui définit les données à inclure avec un événement. | Type complexe TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- TemplateItemType type complexe EventLog
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211518"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="4d24b-105">Type complexe TemplateItemType</span><span class="sxs-lookup"><span data-stu-id="4d24b-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="4d24b-106">Modèle qui définit les données à inclure avec un événement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4d24b-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4d24b-107">Child elements</span></span>



| <span data-ttu-id="4d24b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="4d24b-108">Element</span></span>                                                                   | <span data-ttu-id="4d24b-109">Type</span><span class="sxs-lookup"><span data-stu-id="4d24b-109">Type</span></span>                                                                                 | <span data-ttu-id="4d24b-110">Description</span><span class="sxs-lookup"><span data-stu-id="4d24b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d24b-111">**binaire2**</span><span class="sxs-lookup"><span data-stu-id="4d24b-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="4d24b-112">Réservé à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4d24b-113">**métadonnée**</span><span class="sxs-lookup"><span data-stu-id="4d24b-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="4d24b-114">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="4d24b-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="4d24b-115">Définit un élément de données que vous souhaitez inclure avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4d24b-116">**modélis**</span><span class="sxs-lookup"><span data-stu-id="4d24b-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="4d24b-117">**StructDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="4d24b-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="4d24b-118">Définit une structure qui inclut un ou plusieurs éléments de données que vous souhaitez inclure avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="4d24b-119">Les fournisseurs écrivent la structure en tant qu’objet BLOB et non en tant que membres individuels de la structure.</span><span class="sxs-lookup"><span data-stu-id="4d24b-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="4d24b-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="4d24b-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="4d24b-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="4d24b-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="4d24b-122">Fragment XML utilisé pour restituer les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="4d24b-123">Si vous n’incluez pas le fragment, les données d’événement sont rendues dans l’ordre dans lequel les éléments de données sont définis dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="4d24b-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="4d24b-124">Le contenu de cet élément est tout fragment XML valide.</span><span class="sxs-lookup"><span data-stu-id="4d24b-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="4d24b-125">Le fragment ne doit contenir qu’un seul nœud de niveau supérieur et le nœud de niveau supérieur doit spécifier son propre espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4d24b-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="4d24b-126">Pour référencer un élément de données dans le fragment, définissez le corps du texte d’un nœud dans le fragment sur%*n*, où *n* est l’index de base un des éléments de données de niveau supérieur dans la liste des éléments de données (vous ne pouvez pas référencer les membres d’une structure).</span><span class="sxs-lookup"><span data-stu-id="4d24b-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="4d24b-127">La valeur d’index que vous spécifiez ne doit pas être supérieure au nombre d’éléments de données de niveau supérieur dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="4d24b-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="4d24b-128">Cet élément suit tous les éléments de **données** et de **struct** .</span><span class="sxs-lookup"><span data-stu-id="4d24b-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="4d24b-129">Attributs</span><span class="sxs-lookup"><span data-stu-id="4d24b-129">Attributes</span></span>



| <span data-ttu-id="4d24b-130">Nom</span><span class="sxs-lookup"><span data-stu-id="4d24b-130">Name</span></span> | <span data-ttu-id="4d24b-131">Type</span><span class="sxs-lookup"><span data-stu-id="4d24b-131">Type</span></span>   | <span data-ttu-id="4d24b-132">Description</span><span class="sxs-lookup"><span data-stu-id="4d24b-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d24b-133">name</span><span class="sxs-lookup"><span data-stu-id="4d24b-133">name</span></span> | <span data-ttu-id="4d24b-134">string</span><span class="sxs-lookup"><span data-stu-id="4d24b-134">string</span></span> | <span data-ttu-id="4d24b-135">Réservé à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="4d24b-136">name</span><span class="sxs-lookup"><span data-stu-id="4d24b-136">name</span></span> | <span data-ttu-id="4d24b-137">string</span><span class="sxs-lookup"><span data-stu-id="4d24b-137">string</span></span> | <span data-ttu-id="4d24b-138">Nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="4d24b-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="4d24b-139">tid</span><span class="sxs-lookup"><span data-stu-id="4d24b-139">tid</span></span>  | <span data-ttu-id="4d24b-140">token</span><span class="sxs-lookup"><span data-stu-id="4d24b-140">token</span></span>  | <span data-ttu-id="4d24b-141">Identificateur qui identifie de façon unique le modèle dans la liste des modèles que le fournisseur définit.</span><span class="sxs-lookup"><span data-stu-id="4d24b-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="4d24b-142">Utilisez ce nom pour faire référence au modèle lorsque vous définissez votre définition d’événement.</span><span class="sxs-lookup"><span data-stu-id="4d24b-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4d24b-143">Notes</span><span class="sxs-lookup"><span data-stu-id="4d24b-143">Remarks</span></span>

<span data-ttu-id="4d24b-144">La définition de modèle doit avoir au moins un élément enfant de données ou struct.</span><span class="sxs-lookup"><span data-stu-id="4d24b-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="4d24b-145">Le fournisseur doit écrire les données d’événement dans l’ordre des éléments de données définis dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="4d24b-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="4d24b-146">La taille de tous les éléments de données du modèle doit être inférieure à 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="4d24b-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="4d24b-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="4d24b-147">Examples</span></span>

<span data-ttu-id="4d24b-148">L’exemple suivant montre comment créer une définition de modèle.</span><span class="sxs-lookup"><span data-stu-id="4d24b-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="4d24b-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d24b-149">Requirements</span></span>



| <span data-ttu-id="4d24b-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d24b-150">Requirement</span></span> | <span data-ttu-id="4d24b-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d24b-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d24b-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d24b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4d24b-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d24b-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4d24b-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d24b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4d24b-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d24b-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





