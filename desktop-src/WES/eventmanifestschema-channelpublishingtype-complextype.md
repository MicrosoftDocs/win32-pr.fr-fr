---
title: Type complexe ChannelPublishingType
description: Définit les propriétés de journalisation pour la session utilisée par le canal. | Type complexe ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- ChannelPublishingType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529569"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="b371a-105">Type complexe ChannelPublishingType</span><span class="sxs-lookup"><span data-stu-id="b371a-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="b371a-106">Définit les propriétés de journalisation pour la session utilisée par le canal.</span><span class="sxs-lookup"><span data-stu-id="b371a-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
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

## <a name="child-elements"></a><span data-ttu-id="b371a-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b371a-107">Child elements</span></span>



| <span data-ttu-id="b371a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b371a-108">Element</span></span>                                                                              | <span data-ttu-id="b371a-109">Type</span><span class="sxs-lookup"><span data-stu-id="b371a-109">Type</span></span>                                                              | <span data-ttu-id="b371a-110">Description</span><span class="sxs-lookup"><span data-stu-id="b371a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b371a-111">**Tampon**</span><span class="sxs-lookup"><span data-stu-id="b371a-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="b371a-112">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="b371a-113">Quantité de mémoire, en kilo-octets, à allouer pour chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b371a-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="b371a-114">Si vous vous attendez à un taux d’événements relativement faible, la taille de la mémoire tampon doit être définie sur la taille de la page de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b371a-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="b371a-115">Si le taux d’événements est supposé être relativement élevé, vous devez spécifier une plus grande taille de mémoire tampon et augmenter le nombre maximal de mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="b371a-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="b371a-116">La taille de la mémoire tampon affecte la vitesse à laquelle les tampons sont remplis et doivent être vidés.</span><span class="sxs-lookup"><span data-stu-id="b371a-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="b371a-117">Bien qu’une petite taille de mémoire tampon nécessite moins de mémoire, elle augmente la vitesse à laquelle les tampons doivent être vidés.</span><span class="sxs-lookup"><span data-stu-id="b371a-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="b371a-118">La taille de la mémoire tampon par défaut pour les canaux d’analyse et de débogage est de 4 Ko, et pour admin et opérationnel, il s’agit de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="b371a-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="b371a-119">**clockType**</span><span class="sxs-lookup"><span data-stu-id="b371a-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="b371a-120">Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement.</span><span class="sxs-lookup"><span data-stu-id="b371a-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="b371a-121">Vous pouvez spécifier SystemTime ou QPC.</span><span class="sxs-lookup"><span data-stu-id="b371a-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="b371a-122">SystemTime fournit un horodatage de faible résolution (10 millisecondes), mais est relativement moins onéreux à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b371a-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="b371a-123">La valeur par défaut est SystemTime.</span><span class="sxs-lookup"><span data-stu-id="b371a-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="b371a-124">Le compteur de performance des requêtes (QPC) fournit un horodatage à haute résolution (nanosecondes 100), mais il est relativement coûteux à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b371a-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="b371a-125">Vous devez QPC si vous avez des taux d’événements élevés ou si le consommateur fusionne les événements à partir de mémoires tampons différentes.</span><span class="sxs-lookup"><span data-stu-id="b371a-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="b371a-126">**controlGuid**</span><span class="sxs-lookup"><span data-stu-id="b371a-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="b371a-127">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="b371a-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="b371a-128">Identifie le GUID de session pour une session ETW qui contient des événements WPP.</span><span class="sxs-lookup"><span data-stu-id="b371a-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="b371a-129">Ce paramètre est autorisé uniquement pour les canaux de type Debug.</span><span class="sxs-lookup"><span data-stu-id="b371a-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="b371a-130">Ces canaux ne peuvent pas être entièrement activés avec les mots clés définis sur zéro (0x0000000000000000).</span><span class="sxs-lookup"><span data-stu-id="b371a-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="b371a-131">Ils doivent être activés avec les mots clés définis sur 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b371a-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b371a-132">**fileMax**</span><span class="sxs-lookup"><span data-stu-id="b371a-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="b371a-133">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="b371a-134">Nombre maximal de fois où vous souhaitez que le service crée un nouveau fichier journal lorsque le canal est activé (y compris lorsque l’ordinateur est redémarré).</span><span class="sxs-lookup"><span data-stu-id="b371a-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="b371a-135">Si la valeur est 0 ou 1, le service remplacera le fichier journal chaque fois que le canal est activé et que les événements précédents seront perdus.</span><span class="sxs-lookup"><span data-stu-id="b371a-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="b371a-136">Si la valeur est supérieure à 1, le service crée un nouveau fichier journal chaque fois que le canal est activé afin de conserver les événements.</span><span class="sxs-lookup"><span data-stu-id="b371a-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="b371a-137">La valeur par défaut est 1 et la valeur maximale que vous pouvez spécifier est 16.</span><span class="sxs-lookup"><span data-stu-id="b371a-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="b371a-138">Le service ajoute un nombre décimal à trois chiffres compris entre 0 et fileMax 1 à chaque nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="b371a-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="b371a-139">Par exemple, *nom de fichier*. etl.xxx, où xxx est le nombre décimal à trois chiffres.</span><span class="sxs-lookup"><span data-stu-id="b371a-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="b371a-140">Les fichiers se trouvent dans les journaux% windir% \\ system32 \\ winevt \\ .</span><span class="sxs-lookup"><span data-stu-id="b371a-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="b371a-141">**mot**</span><span class="sxs-lookup"><span data-stu-id="b371a-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="b371a-142">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="b371a-143">Masque de réécriture qui détermine la catégorie des événements écrits dans le canal.</span><span class="sxs-lookup"><span data-stu-id="b371a-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="b371a-144">Si la valeur de l’attribut **Keywords** est 0, tous les événements écrits par le fournisseur sont écrits dans le canal ; Sinon, seuls les événements qui ont défini un mot clé inclus dans le masque de masque des **Mots clés** sont écrits dans le canal.</span><span class="sxs-lookup"><span data-stu-id="b371a-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="b371a-145">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="b371a-145">The default is 0.</span></span><br/> <span data-ttu-id="b371a-146">Les canaux de débogage dont l’attribut controlGuid est défini doivent définir l’attribut **Keywords** sur 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b371a-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="b371a-147">La session transmet la valeur des mots clés au fournisseur lorsqu’il active le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b371a-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="b371a-148">**latence**</span><span class="sxs-lookup"><span data-stu-id="b371a-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="b371a-149">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="b371a-150">Délai d’attente avant le vidage des mémoires tampons, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="b371a-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="b371a-151">Si la valeur est zéro, ETW vide les mémoires tampons dès qu’elles sont complètes.</span><span class="sxs-lookup"><span data-stu-id="b371a-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="b371a-152">Si la valeur est différente de zéro, ETW vide toutes les mémoires tampons qui contiennent des événements basés sur la valeur même si la mémoire tampon n’est pas saturée.</span><span class="sxs-lookup"><span data-stu-id="b371a-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="b371a-153">En règle générale, vous souhaitez vider les mémoires tampons uniquement lorsqu’elles sont complètes.</span><span class="sxs-lookup"><span data-stu-id="b371a-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="b371a-154">Forcer le vidage des mémoires tampons peut augmenter la taille du fichier journal avec un espace de mémoire tampon non rempli.</span><span class="sxs-lookup"><span data-stu-id="b371a-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="b371a-155">La valeur par défaut est 1 seconde pour les journaux d’administration et les journaux des opérations et 5 secondes pour les journaux d’analyse et de débogage.</span><span class="sxs-lookup"><span data-stu-id="b371a-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="b371a-156">**niveau**</span><span class="sxs-lookup"><span data-stu-id="b371a-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="b371a-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="b371a-158">Niveau de gravité des événements à écrire dans le canal.</span><span class="sxs-lookup"><span data-stu-id="b371a-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="b371a-159">Le service écrit des événements dans le canal qui ont une valeur de niveau inférieure ou égale à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b371a-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="b371a-160">La valeur par défaut est 0, ce qui signifie que enregistre les événements avec n’importe quelle valeur de niveau.</span><span class="sxs-lookup"><span data-stu-id="b371a-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="b371a-161">La session transmet la valeur de niveau au fournisseur lorsqu’il active le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b371a-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="b371a-162">**maxBuffers**</span><span class="sxs-lookup"><span data-stu-id="b371a-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="b371a-163">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="b371a-164">Nombre maximal de mémoires tampons à allouer pour la session.</span><span class="sxs-lookup"><span data-stu-id="b371a-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="b371a-165">En général, cette valeur est le nombre minimal de mémoires tampons plus vingt.</span><span class="sxs-lookup"><span data-stu-id="b371a-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="b371a-166">Cette valeur doit être supérieure ou égale à la valeur spécifiée pour minBuffers.</span><span class="sxs-lookup"><span data-stu-id="b371a-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="b371a-167">Le nombre maximal par défaut de mémoires tampons pour les canaux d’analyse et de débogage est de 10 Ko, et pour admin et opérationnel, il s’agit de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="b371a-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="b371a-168">**minBuffers**</span><span class="sxs-lookup"><span data-stu-id="b371a-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="b371a-169">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b371a-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="b371a-170">Nombre minimal de mémoires tampons à allouer pour la session.</span><span class="sxs-lookup"><span data-stu-id="b371a-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="b371a-171">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="b371a-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="b371a-172">**sidType**</span><span class="sxs-lookup"><span data-stu-id="b371a-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="b371a-173">Détermine s’il faut inclure un identificateur de sécurité (SID) du principal avec chaque événement écrit dans le canal.</span><span class="sxs-lookup"><span data-stu-id="b371a-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="b371a-174">Pour inclure le SID avec l’événement, définissez cet attribut sur « publication ».</span><span class="sxs-lookup"><span data-stu-id="b371a-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="b371a-175">Le SID est défini en fonction de l’identité du thread au moment de l’écriture de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b371a-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="b371a-176">Si vous ne souhaitez pas inclure le SID avec l’événement, définissez cet attribut sur « None ».</span><span class="sxs-lookup"><span data-stu-id="b371a-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="b371a-177">La valeur par défaut est « publication ».</span><span class="sxs-lookup"><span data-stu-id="b371a-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="b371a-178">Notes</span><span class="sxs-lookup"><span data-stu-id="b371a-178">Remarks</span></span>

<span data-ttu-id="b371a-179">Vous pouvez spécifier ces informations de publication pour les types de canaux d’analyse et de débogage, ou pour n’importe quel canal qui spécifie l’isolation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b371a-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="b371a-180">Bien que vous puissiez spécifier le niveau et les mots clés, vous devez considérer qu’il s’agit des seuls événements que vous recevrez du fournisseur pour ce canal.</span><span class="sxs-lookup"><span data-stu-id="b371a-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="b371a-181">Quand une mémoire tampon est saturée, ETW vide la mémoire tampon dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b371a-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="b371a-182">Si les mémoires tampons sont remplies plus rapidement qu’elles ne peuvent être vidées, de nouvelles mémoires tampons sont allouées et ajoutées au pool de mémoires tampons de la session, jusqu’au nombre maximal spécifié.</span><span class="sxs-lookup"><span data-stu-id="b371a-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="b371a-183">Au-delà de cette limite, la session ignore les événements entrants jusqu’à ce qu’une mémoire tampon soit disponible.</span><span class="sxs-lookup"><span data-stu-id="b371a-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="b371a-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b371a-184">Requirements</span></span>



| <span data-ttu-id="b371a-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b371a-185">Requirement</span></span> | <span data-ttu-id="b371a-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="b371a-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b371a-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b371a-187">Minimum supported client</span></span><br/> | <span data-ttu-id="b371a-188">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b371a-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b371a-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b371a-189">Minimum supported server</span></span><br/> | <span data-ttu-id="b371a-190">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b371a-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





