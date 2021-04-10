---
title: Type complexe ChannelLoggingType
description: Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et s’il est séquentiel ou circulaire. | Type complexe ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116154"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="9c8d2-105">Type complexe ChannelLoggingType</span><span class="sxs-lookup"><span data-stu-id="9c8d2-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="9c8d2-106">Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et s’il est séquentiel ou circulaire.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9c8d2-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9c8d2-107">Child elements</span></span>



| <span data-ttu-id="9c8d2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="9c8d2-108">Element</span></span>                                                                         | <span data-ttu-id="9c8d2-109">Type</span><span class="sxs-lookup"><span data-stu-id="9c8d2-109">Type</span></span>                                                              | <span data-ttu-id="9c8d2-110">Description</span><span class="sxs-lookup"><span data-stu-id="9c8d2-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c8d2-111">**La sauvegarde automatique**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="9c8d2-112">boolean</span><span class="sxs-lookup"><span data-stu-id="9c8d2-112">boolean</span></span>                                                           | <span data-ttu-id="9c8d2-113">Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="9c8d2-114">Affectez la valeur **true** pour demander que le service crée un nouveau fichier lorsque le fichier journal atteint sa taille maximale ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="9c8d2-115">Vous ne pouvez définir la [**sauvegarde autosauvegarde**](eventmanifestschema-autobackup-channelloggingtype-element.md) que sur **true** si la [**rétention**](eventmanifestschema-retention-channelloggingtype-element.md) est définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="9c8d2-116">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-116">The default is **false**.</span></span><br/> <span data-ttu-id="9c8d2-117">Il n’existe aucune limite au nombre de fichiers de sauvegarde que le service peut créer (limité uniquement par l’espace disque disponible).</span><span class="sxs-lookup"><span data-stu-id="9c8d2-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="9c8d2-118">Les noms des fichiers de sauvegarde se présentent sous la forme Archive-*channelName* - *timestamp*. evtx et se trouvent dans le dossier% windir% \\ system32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="9c8d2-119">**maxSize**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="9c8d2-120">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="9c8d2-121">Taille maximale, en octets, du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="9c8d2-122">La valeur par défaut (et la valeur minimale) est 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="9c8d2-123">Si la taille du journal physique est inférieure à la taille maximale configurée et que l’espace supplémentaire est requis dans le journal pour stocker les événements, le service alloue un autre bloc d’espace même si la taille physique résultante du journal est supérieure à la taille maximale configurée.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="9c8d2-124">Le service alloue des blocs de 1 Mo, de sorte que la taille physique peut croître jusqu’à 1 Mo de plus que la taille maximale configurée.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9c8d2-125">**fixation**</span><span class="sxs-lookup"><span data-stu-id="9c8d2-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="9c8d2-126">boolean</span><span class="sxs-lookup"><span data-stu-id="9c8d2-126">boolean</span></span>                                                           | <span data-ttu-id="9c8d2-127">Détermine si le fichier journal est un fichier journal séquentiel ou circulaire.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="9c8d2-128">Affectez la valeur **true** à un fichier journal séquentiel et la **valeur false** à un fichier journal circulaire.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="9c8d2-129">La valeur par défaut est **false** pour les types de canaux d’administration et opérationnels, et **true** pour les types de canaux d’analyse et de débogage.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="9c8d2-130">Pour interroger un journal circulaire, vous devez d’abord désactiver le canal.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="9c8d2-131">Notes</span><span class="sxs-lookup"><span data-stu-id="9c8d2-131">Remarks</span></span>

<span data-ttu-id="9c8d2-132">Vous pouvez spécifier l’attribut **MaxSize** pour tout type de canal.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="9c8d2-133">Vous pouvez spécifier l’attribut **Autobackup** uniquement pour les types de canaux d’administration et opérationnels.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="9c8d2-134">Vous pouvez affecter la valeur false (journalisation circulaire) à l’attribut de **rétention** pour les types de canaux opérationnels et d’administration.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="9c8d2-135">Vous pouvez définir l’attribut de **rétention** sur false (enregistrement circulaire) pour les types de canaux d’analyse et de débogage, mais pour afficher les événements dans le observateur d’événements Windows, vous devez d’abord désactiver le canal.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="9c8d2-136">Notez que lorsque vous réactivez le canal, les événements sont supprimés du canal.</span><span class="sxs-lookup"><span data-stu-id="9c8d2-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8d2-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c8d2-137">Requirements</span></span>



| <span data-ttu-id="9c8d2-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c8d2-138">Requirement</span></span> | <span data-ttu-id="9c8d2-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c8d2-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c8d2-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c8d2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8d2-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c8d2-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c8d2-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c8d2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8d2-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c8d2-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





