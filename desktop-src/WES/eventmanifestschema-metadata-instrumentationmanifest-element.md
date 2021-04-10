---
title: Élément Metadata (instrumentationManifest)
description: Contient des valeurs globales que vous pouvez référencer dans d’autres manifestes.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- EventLog (élément de métadonnées)
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102932"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="9d4a4-104">Élément Metadata (instrumentationManifest)</span><span class="sxs-lookup"><span data-stu-id="9d4a4-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="9d4a4-105">Contient des valeurs globales que vous pouvez référencer dans d’autres manifestes.</span><span class="sxs-lookup"><span data-stu-id="9d4a4-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="9d4a4-106">Pour obtenir un exemple, consultez le fichier Winmeta.xml inclus dans le \\ dossier include du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="9d4a4-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="9d4a4-107">L’élément **Metadata** est défini par l’élément [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d4a4-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d4a4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9d4a4-108">Remarks</span></span>

<span data-ttu-id="9d4a4-109">Bien que vous puissiez créer un manifeste qui contient une section de métadonnées, le service ne l’utilise pas. les seules métadonnées reconnues par le service sont les métadonnées trouvées dans le fichier Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="9d4a4-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d4a4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d4a4-110">Requirements</span></span>



| <span data-ttu-id="9d4a4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d4a4-111">Requirement</span></span> | <span data-ttu-id="9d4a4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d4a4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d4a4-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d4a4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4a4-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d4a4-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d4a4-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d4a4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4a4-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d4a4-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d4a4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d4a4-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d4a4-118">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="9d4a4-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="9d4a4-119">**instrumentationManifest**</span><span class="sxs-lookup"><span data-stu-id="9d4a4-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





