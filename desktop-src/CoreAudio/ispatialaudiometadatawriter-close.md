---
description: Effectue toutes les opérations nécessaires sur la mémoire tampon des métadonnées et libère l’objet ISpatialAudioMetadataItems spécifié.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'ISpatialAudioMetadataWriter :: Close, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111195"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="68ca5-103">ISpatialAudioMetadataWriter :: Close, méthode</span><span class="sxs-lookup"><span data-stu-id="68ca5-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="68ca5-104">Effectue toutes les opérations nécessaires sur la mémoire tampon des métadonnées et libère l’objet [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) spécifié.</span><span class="sxs-lookup"><span data-stu-id="68ca5-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ca5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68ca5-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="68ca5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68ca5-106">Parameters</span></span>

<span data-ttu-id="68ca5-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="68ca5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68ca5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68ca5-108">Return value</span></span>

<span data-ttu-id="68ca5-109">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68ca5-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="68ca5-110">En cas d’échec, les codes de retour possibles incluent, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="68ca5-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="68ca5-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="68ca5-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="68ca5-112">Description</span><span class="sxs-lookup"><span data-stu-id="68ca5-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68ca5-113"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ aucun \_ élément \_ ouvert**</dt></span><span class="sxs-lookup"><span data-stu-id="68ca5-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="68ca5-114">Le [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) fourni n’a pas été ouvert avec un appel à [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span><span class="sxs-lookup"><span data-stu-id="68ca5-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="68ca5-115"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ aucun \_ élément \_ écrit**</dt></span><span class="sxs-lookup"><span data-stu-id="68ca5-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="68ca5-116">Aucun élément de métadonnées n’a été écrit dans le [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fourni.</span><span class="sxs-lookup"><span data-stu-id="68ca5-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="68ca5-117"><dt>**l' \_ élément SPTLAUD MD \_ CLNT \_ E \_ \_ doit \_ avoir des \_ commandes**</dt></span><span class="sxs-lookup"><span data-stu-id="68ca5-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="68ca5-118">Aucune commande de métadonnées n’a été écrite dans le [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fourni.</span><span class="sxs-lookup"><span data-stu-id="68ca5-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="68ca5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68ca5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ca5-120">**ISpatialAudioMetadataWriter**</span><span class="sxs-lookup"><span data-stu-id="68ca5-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




