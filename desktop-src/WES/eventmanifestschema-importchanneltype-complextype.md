---
title: Type complexe ImportChannelType
description: Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- ImportChannelType type complexe EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103588"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="897c6-104">Type complexe ImportChannelType</span><span class="sxs-lookup"><span data-stu-id="897c6-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="897c6-105">Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="897c6-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="897c6-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="897c6-106">Attributes</span></span>



| <span data-ttu-id="897c6-107">Nom</span><span class="sxs-lookup"><span data-stu-id="897c6-107">Name</span></span>   | <span data-ttu-id="897c6-108">Type</span><span class="sxs-lookup"><span data-stu-id="897c6-108">Type</span></span>                                                              | <span data-ttu-id="897c6-109">Description</span><span class="sxs-lookup"><span data-stu-id="897c6-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="897c6-110">enfants</span><span class="sxs-lookup"><span data-stu-id="897c6-110">chid</span></span>   | <span data-ttu-id="897c6-111">token</span><span class="sxs-lookup"><span data-stu-id="897c6-111">token</span></span>                                                             | <span data-ttu-id="897c6-112">Identificateur qui identifie de façon unique le canal dans la liste des canaux que le fournisseur définit ou importe.</span><span class="sxs-lookup"><span data-stu-id="897c6-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="897c6-113">Utilisez cette valeur lors du référencement de ce canal dans une définition d’événement.</span><span class="sxs-lookup"><span data-stu-id="897c6-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="897c6-114">Si vous ne spécifiez pas d’identificateur de canal, utilisez le nom du canal pour référencer ce canal dans une définition d’événement.</span><span class="sxs-lookup"><span data-stu-id="897c6-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="897c6-115">name</span><span class="sxs-lookup"><span data-stu-id="897c6-115">name</span></span>   | <span data-ttu-id="897c6-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="897c6-116">anyURI</span></span>                                                            | <span data-ttu-id="897c6-117">Nom du canal à importer.</span><span class="sxs-lookup"><span data-stu-id="897c6-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="897c6-118">symbole</span><span class="sxs-lookup"><span data-stu-id="897c6-118">symbol</span></span> | [<span data-ttu-id="897c6-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="897c6-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="897c6-120">Symbole à utiliser pour référencer le canal dans votre application.</span><span class="sxs-lookup"><span data-stu-id="897c6-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="897c6-121">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le canal dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="897c6-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="897c6-122">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="897c6-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="897c6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="897c6-123">Remarks</span></span>

<span data-ttu-id="897c6-124">Le manifeste qui a défini le canal importé doit être installé avant que votre fournisseur n’écrive des événements ; dans le cas contraire, les événements ne peuvent pas être écrits dans le canal (l’opération d’écriture a abouti, les événements ne sont tout simplement pas écrits sur le canal).</span><span class="sxs-lookup"><span data-stu-id="897c6-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="897c6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="897c6-125">Requirements</span></span>



| <span data-ttu-id="897c6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="897c6-126">Requirement</span></span> | <span data-ttu-id="897c6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="897c6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="897c6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="897c6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="897c6-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="897c6-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="897c6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="897c6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="897c6-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="897c6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





