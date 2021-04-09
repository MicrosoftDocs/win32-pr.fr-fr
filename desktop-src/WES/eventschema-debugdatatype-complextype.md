---
title: Type complexe DebugDataType
description: Définit les données qui peuvent être journalisées pour les événements du préprocesseur de trace logiciel Windows (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType type complexe EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032285"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="e1de8-104">Type complexe DebugDataType</span><span class="sxs-lookup"><span data-stu-id="e1de8-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="e1de8-105">Définit les données qui peuvent être journalisées pour les événements du préprocesseur de trace logiciel Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="e1de8-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e1de8-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e1de8-106">Child elements</span></span>



| <span data-ttu-id="e1de8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="e1de8-107">Element</span></span>                                                                    | <span data-ttu-id="e1de8-108">Type</span><span class="sxs-lookup"><span data-stu-id="e1de8-108">Type</span></span>        | <span data-ttu-id="e1de8-109">Description</span><span class="sxs-lookup"><span data-stu-id="e1de8-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1de8-110">**Composant**</span><span class="sxs-lookup"><span data-stu-id="e1de8-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="e1de8-111">string</span><span class="sxs-lookup"><span data-stu-id="e1de8-111">string</span></span>      | <span data-ttu-id="e1de8-112">Nom du composant qui a consigné le message de trace.</span><span class="sxs-lookup"><span data-stu-id="e1de8-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="e1de8-113">**FileLine**</span><span class="sxs-lookup"><span data-stu-id="e1de8-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="e1de8-114">string</span><span class="sxs-lookup"><span data-stu-id="e1de8-114">string</span></span>      | <span data-ttu-id="e1de8-115">Nom du fichier source et ligne dans le fichier source qui a consigné le message de trace.</span><span class="sxs-lookup"><span data-stu-id="e1de8-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="e1de8-116">**FlagsName**</span><span class="sxs-lookup"><span data-stu-id="e1de8-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="e1de8-117">string</span><span class="sxs-lookup"><span data-stu-id="e1de8-117">string</span></span>      | <span data-ttu-id="e1de8-118">Valeur d’indicateur passée au fournisseur lorsqu’il a été activé.</span><span class="sxs-lookup"><span data-stu-id="e1de8-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="e1de8-119">**Function**</span><span class="sxs-lookup"><span data-stu-id="e1de8-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="e1de8-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e1de8-120">unsignedInt</span></span> | <span data-ttu-id="e1de8-121">Nom de la fonction qui a consigné le message de trace.</span><span class="sxs-lookup"><span data-stu-id="e1de8-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="e1de8-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="e1de8-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="e1de8-123">string</span><span class="sxs-lookup"><span data-stu-id="e1de8-123">string</span></span>      | <span data-ttu-id="e1de8-124">Valeur de niveau passée au fournisseur lorsqu’il a été activé.</span><span class="sxs-lookup"><span data-stu-id="e1de8-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="e1de8-125">**Message**</span><span class="sxs-lookup"><span data-stu-id="e1de8-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="e1de8-126">string</span><span class="sxs-lookup"><span data-stu-id="e1de8-126">string</span></span>      | <span data-ttu-id="e1de8-127">Chaîne du message.</span><span class="sxs-lookup"><span data-stu-id="e1de8-127">The message string.</span></span> <span data-ttu-id="e1de8-128">Le code XML contient cet élément si l’événement WPP a spécifié le champ FormattedString.</span><span class="sxs-lookup"><span data-stu-id="e1de8-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="e1de8-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e1de8-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="e1de8-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e1de8-130">unsignedInt</span></span> | <span data-ttu-id="e1de8-131">Numéro de séquence local ou global du message de trace.</span><span class="sxs-lookup"><span data-stu-id="e1de8-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="e1de8-132">**Sous-composant**</span><span class="sxs-lookup"><span data-stu-id="e1de8-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="e1de8-133">string</span><span class="sxs-lookup"><span data-stu-id="e1de8-133">string</span></span>      | <span data-ttu-id="e1de8-134">Nom du sous-composant qui a consigné le message de trace.</span><span class="sxs-lookup"><span data-stu-id="e1de8-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="e1de8-135">Notes</span><span class="sxs-lookup"><span data-stu-id="e1de8-135">Remarks</span></span>

<span data-ttu-id="e1de8-136">Les éléments sont inclus uniquement si le fournisseur définit la \_ \_ variable d’environnement% préfixe de format de trace% pour les inclure.</span><span class="sxs-lookup"><span data-stu-id="e1de8-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="e1de8-137">Pour plus d’informations sur ces éléments, consultez préfixe du message de suivi.</span><span class="sxs-lookup"><span data-stu-id="e1de8-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1de8-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1de8-138">Requirements</span></span>



| <span data-ttu-id="e1de8-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1de8-139">Requirement</span></span> | <span data-ttu-id="e1de8-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1de8-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e1de8-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1de8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e1de8-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1de8-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e1de8-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1de8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e1de8-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1de8-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





