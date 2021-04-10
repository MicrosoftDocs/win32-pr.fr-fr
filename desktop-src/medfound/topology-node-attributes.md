---
description: Attributs de nœud de topologie
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Attributs de nœud de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951617"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="a066a-103">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="a066a-103">Topology Node Attributes</span></span>

<span data-ttu-id="a066a-104">Les attributs suivants s’appliquent aux nœuds de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="a066a-105">Attributs généraux de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="a066a-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="a066a-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="a066a-106">Attribute</span></span>                                                                       | <span data-ttu-id="a066a-107">Description</span><span class="sxs-lookup"><span data-stu-id="a066a-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a066a-108">**\_méthode de \_ connexion MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="a066a-109">Spécifie comment le chargeur de topologie connecte ce nœud de topologie et si ce nœud est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a066a-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="a066a-110">**\_DÉcodeur TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="a066a-111">Spécifie si l’objet d’un nœud topologie est un décodeur.</span><span class="sxs-lookup"><span data-stu-id="a066a-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="a066a-112">**\_déchiffreur MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="a066a-113">Spécifie si l’objet sous-jacent d’un nœud topologie est un déchiffreur.</span><span class="sxs-lookup"><span data-stu-id="a066a-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="a066a-114">**TOPONODE MF à \_ \_ Ignorer**</span><span class="sxs-lookup"><span data-stu-id="a066a-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="a066a-115">Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="a066a-116">**\_erreur TOPONODE \_ MF \_ MAJORTYPE**</span><span class="sxs-lookup"><span data-stu-id="a066a-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="a066a-117">Contient le type de média principal pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="a066a-118">Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a066a-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="a066a-119">**\_sous- \_ type d’erreur TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="a066a-120">Contient le sous-type de média pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="a066a-121">Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a066a-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="a066a-122">**MF \_ TOPONODE \_ ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="a066a-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="a066a-123">Contient le code d’erreur de l’échec de connexion le plus récent pour ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="a066a-124">**\_TOPONODE MF \_ verrouillé**</span><span class="sxs-lookup"><span data-stu-id="a066a-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="a066a-125">Spécifie si les types de média peuvent être modifiés sur ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="a066a-126">**\_Mark MF TOPONODE \_ \_ ici**</span><span class="sxs-lookup"><span data-stu-id="a066a-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="a066a-127">Spécifie si le pipeline applique la marque dans ce nœud.</span><span class="sxs-lookup"><span data-stu-id="a066a-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="a066a-128">**\_MARKOUT TOPONODE \_ MF \_ ici**</span><span class="sxs-lookup"><span data-stu-id="a066a-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="a066a-129">Spécifie si le pipeline applique le marquage sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="a066a-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="a066a-130">Attributs du nœud source</span><span class="sxs-lookup"><span data-stu-id="a066a-130">Source Node Attributes</span></span>



| <span data-ttu-id="a066a-131">Attribut</span><span class="sxs-lookup"><span data-stu-id="a066a-131">Attribute</span></span>                                                                                       | <span data-ttu-id="a066a-132">Description</span><span class="sxs-lookup"><span data-stu-id="a066a-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a066a-133">**\_MEDIASTART TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="a066a-134">Spécifie l’heure de début d’une présentation, par rapport au démarrage du fichier source du média, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a066a-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="a066a-135">**\_MEDIASTOP TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="a066a-136">Spécifie l’heure d’arrêt d’une présentation, par rapport au démarrage du fichier source du média, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a066a-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="a066a-137">**\_descripteur de présentation TOPONODE MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="a066a-138">Contient un pointeur vers le descripteur de présentation pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="a066a-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="a066a-139">**\_séquence d’TOPONODE de \_ SÉQUENCEs MF \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="a066a-140">Spécifie l’élément qui contient un nœud source.</span><span class="sxs-lookup"><span data-stu-id="a066a-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="a066a-141">**\_source TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="a066a-142">Contient un pointeur vers la source du média associée à un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="a066a-143">**\_descripteur de flux TOPONODE MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="a066a-144">Contient un pointeur vers le descripteur de flux pour la source du média.</span><span class="sxs-lookup"><span data-stu-id="a066a-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="a066a-145">**\_ID de \_ WORKQUEUE \_ TOPONODE MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="a066a-146">Spécifie une file d’attente de travail pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="a066a-147">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS, \_ classe**</span><span class="sxs-lookup"><span data-stu-id="a066a-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="a066a-148">Spécifie une tâche du service Planificateur de classes multimédias (MMCSS) pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="a066a-149">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="a066a-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="a066a-150">Spécifie un identificateur de tâche MMCSS pour un nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="a066a-151">Attributs du nœud transformer</span><span class="sxs-lookup"><span data-stu-id="a066a-151">Transform Node Attributes</span></span>



| <span data-ttu-id="a066a-152">Attribut</span><span class="sxs-lookup"><span data-stu-id="a066a-152">Attribute</span></span>                                                                             | <span data-ttu-id="a066a-153">Description</span><span class="sxs-lookup"><span data-stu-id="a066a-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a066a-154">**\_D3DAWARE TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="a066a-155">Spécifie si la transformation associée à un nœud de topologie prend en charge l’accélération vidéo DirectX (DXVA)</span><span class="sxs-lookup"><span data-stu-id="a066a-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="a066a-156">**\_drainage TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="a066a-157">Spécifie quand une transformation est vidée.</span><span class="sxs-lookup"><span data-stu-id="a066a-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="a066a-158">**\_vidage TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="a066a-159">Spécifie quand une transformation est vidée.</span><span class="sxs-lookup"><span data-stu-id="a066a-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="a066a-160">**\_ID d’TOPONODE de \_ transformation MF \_**</span><span class="sxs-lookup"><span data-stu-id="a066a-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="a066a-161">Identificateur de classe (CLSID) de la transformation associée à ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="a066a-162">Attributs du nœud de sortie</span><span class="sxs-lookup"><span data-stu-id="a066a-162">Output Node Attributes</span></span>



| <span data-ttu-id="a066a-163">Attribut</span><span class="sxs-lookup"><span data-stu-id="a066a-163">Attribute</span></span>                                                                                  | <span data-ttu-id="a066a-164">Description</span><span class="sxs-lookup"><span data-stu-id="a066a-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a066a-165">**\_TOPONODE de \_ désactiver le \_ préroll MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="a066a-166">Spécifie si la session multimédia utilise le préroll sur le récepteur multimédia représenté par ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="a066a-167">**\_TOPONODE \_ de l’infermeture MF en cas \_ de \_ suppression**</span><span class="sxs-lookup"><span data-stu-id="a066a-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="a066a-168">Spécifie si la session multimédia arrête le récepteur multimédia lorsque le nœud de sortie est supprimé de la topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="a066a-169">**\_TOPONODE de \_ Vitesse MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="a066a-170">Spécifie si le récepteur multimédia associé à ce nœud de topologie est sans débit.</span><span class="sxs-lookup"><span data-stu-id="a066a-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="a066a-171">**\_STREAMID TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="a066a-172">Identificateur de flux du récepteur de flux associé à ce nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="a066a-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="a066a-173">Attributs du nœud tee</span><span class="sxs-lookup"><span data-stu-id="a066a-173">Tee Node Attributes</span></span>



| <span data-ttu-id="a066a-174">Attribut</span><span class="sxs-lookup"><span data-stu-id="a066a-174">Attribute</span></span>                                                                  | <span data-ttu-id="a066a-175">Description</span><span class="sxs-lookup"><span data-stu-id="a066a-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="a066a-176">**\_PrimaryOutput, car TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a066a-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="a066a-177">Indique quelle sortie est la sortie principale sur un nœud tee.</span><span class="sxs-lookup"><span data-stu-id="a066a-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a066a-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a066a-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a066a-179">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="a066a-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="a066a-180">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a066a-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a066a-181">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="a066a-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



