---
description: Attributs du descripteur de flux
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Attributs du descripteur de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753844"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="10bfe-103">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="10bfe-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="10bfe-104">Attributs courants du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="10bfe-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="10bfe-105">Les attributs suivants s’appliquent aux descripteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="10bfe-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="10bfe-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="10bfe-106">Attribute</span></span>                                                   | <span data-ttu-id="10bfe-107">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="10bfe-108">**\_langage SD \_ MF**</span><span class="sxs-lookup"><span data-stu-id="10bfe-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="10bfe-109">Spécifie la langue d’un flux.</span><span class="sxs-lookup"><span data-stu-id="10bfe-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="10bfe-110">MF SD s’excluant \_ \_ mutuellement \_</span><span class="sxs-lookup"><span data-stu-id="10bfe-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="10bfe-111">Spécifie si un flux s’exclut mutuellement avec d’autres flux du même type.</span><span class="sxs-lookup"><span data-stu-id="10bfe-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="10bfe-112">**\_protégé SD \_ sécurisé**</span><span class="sxs-lookup"><span data-stu-id="10bfe-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="10bfe-113">Spécifie si un flux de données contient du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="10bfe-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="10bfe-114">\_nom du \_ flux \_ SD MF</span><span class="sxs-lookup"><span data-stu-id="10bfe-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="10bfe-115">Contient le nom d’un flux.</span><span class="sxs-lookup"><span data-stu-id="10bfe-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="10bfe-116">Attributs du descripteur de flux ASF-Specific</span><span class="sxs-lookup"><span data-stu-id="10bfe-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="10bfe-117">Les attributs suivants s’appliquent aux descripteurs de flux pour les fichiers ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="10bfe-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="10bfe-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="10bfe-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="10bfe-119">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10bfe-120">**\_bufferSize SD \_ ASF \_ EXTSTRMPROP \_ Moy \_ .**</span><span class="sxs-lookup"><span data-stu-id="10bfe-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="10bfe-121">Spécifie la taille moyenne de la mémoire tampon nécessaire pour un flux dans un fichier ASF, en octets.</span><span class="sxs-lookup"><span data-stu-id="10bfe-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="10bfe-122">**\_vitesse de \_ \_ \_ transmission moyenne des \_ données EXTSTRMPROP \_ MF SD ASF**</span><span class="sxs-lookup"><span data-stu-id="10bfe-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="10bfe-123">Spécifie la vitesse moyenne de transmission de données d’un flux dans un fichier ASF, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="10bfe-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="10bfe-124">**\_ID de \_ \_ langue EXTSTRMPROP \_ \_ MF \_ SD ASF**</span><span class="sxs-lookup"><span data-stu-id="10bfe-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="10bfe-125">Spécifie la langue utilisée par un flux dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="10bfe-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="10bfe-126">**\_bufferSize SD \_ \_ EXTSTRMPROP ASF \_ Max \_ .**</span><span class="sxs-lookup"><span data-stu-id="10bfe-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="10bfe-127">Spécifie la taille maximale de la mémoire tampon nécessaire pour un flux dans un fichier ASF, en octets.</span><span class="sxs-lookup"><span data-stu-id="10bfe-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="10bfe-128">**\_vitesse de \_ \_ transmission de \_ \_ données Max \_ . ASF EXTSTRMPROP ASF**</span><span class="sxs-lookup"><span data-stu-id="10bfe-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="10bfe-129">Spécifie la vitesse de transmission maximale de données d’un flux dans un fichier ASF, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="10bfe-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="10bfe-130">**\_modèle de \_ \_ conformité des appareils de métadonnées ASF SD ASF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="10bfe-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="10bfe-131">Spécifie le modèle de conformité de périphérique pour un flux de données dans un fichier ASF, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="10bfe-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="10bfe-132">**\_vitesse de \_ \_ transmission de STREAMBITRATES MF SD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="10bfe-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="10bfe-133">Spécifie la vitesse de transmission moyenne d’un flux dans un fichier ASF, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="10bfe-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="10bfe-134">Attributs du descripteur du flux de source du média SAMI</span><span class="sxs-lookup"><span data-stu-id="10bfe-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="10bfe-135">L’attribut suivant s’applique au descripteur de flux pour la source du média SAMI.</span><span class="sxs-lookup"><span data-stu-id="10bfe-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="10bfe-136">Attribut</span><span class="sxs-lookup"><span data-stu-id="10bfe-136">Attribute</span></span>                                                       | <span data-ttu-id="10bfe-137">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10bfe-138">**PP \_ SD \_ ( \_ langage sami)**</span><span class="sxs-lookup"><span data-stu-id="10bfe-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="10bfe-139">Contient le nom du langage SAMI (Synchronized Accessible Media Interchange) qui est défini pour le flux.</span><span class="sxs-lookup"><span data-stu-id="10bfe-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="10bfe-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10bfe-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10bfe-141">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="10bfe-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="10bfe-142">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10bfe-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



