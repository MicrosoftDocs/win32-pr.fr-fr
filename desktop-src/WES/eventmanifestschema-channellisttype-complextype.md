---
title: Type complexe ChannelListType
description: Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements. | Type complexe ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- ChannelListType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543016"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="16fc4-105">Type complexe ChannelListType</span><span class="sxs-lookup"><span data-stu-id="16fc4-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="16fc4-106">Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements.</span><span class="sxs-lookup"><span data-stu-id="16fc4-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="16fc4-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="16fc4-107">Child elements</span></span>



| <span data-ttu-id="16fc4-108">Élément</span><span class="sxs-lookup"><span data-stu-id="16fc4-108">Element</span></span>                                                                            | <span data-ttu-id="16fc4-109">Type</span><span class="sxs-lookup"><span data-stu-id="16fc4-109">Type</span></span>                                                                           | <span data-ttu-id="16fc4-110">Description</span><span class="sxs-lookup"><span data-stu-id="16fc4-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16fc4-111">**couche**</span><span class="sxs-lookup"><span data-stu-id="16fc4-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="16fc4-112">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="16fc4-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="16fc4-113">Définit un canal dans lequel les événements peuvent être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="16fc4-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="16fc4-114">**importChannel**</span><span class="sxs-lookup"><span data-stu-id="16fc4-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="16fc4-115">**ImportChannelType**</span><span class="sxs-lookup"><span data-stu-id="16fc4-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="16fc4-116">Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="16fc4-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="16fc4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="16fc4-117">Remarks</span></span>

<span data-ttu-id="16fc4-118">Vous pouvez spécifier jusqu’à huit canaux (n’importe quelle combinaison de canaux ou canaux importés que vous définissez).</span><span class="sxs-lookup"><span data-stu-id="16fc4-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="16fc4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16fc4-119">Requirements</span></span>



| <span data-ttu-id="16fc4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16fc4-120">Requirement</span></span> | <span data-ttu-id="16fc4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="16fc4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16fc4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16fc4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16fc4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16fc4-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="16fc4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16fc4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16fc4-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16fc4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





