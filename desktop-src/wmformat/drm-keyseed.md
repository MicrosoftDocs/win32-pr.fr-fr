---
title: DRM_KeySeed
description: La \_ propriété DRM keyseed contient la valeur de départ de clé qui sera utilisée conjointement avec le KeyId pour créer la clé.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- Format Windows Media DRM_KeySeed
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106510451"
---
# <a name="drm_keyseed"></a><span data-ttu-id="a2f9c-104">Keyseed DRM \_</span><span class="sxs-lookup"><span data-stu-id="a2f9c-104">DRM\_KeySeed</span></span>

<span data-ttu-id="a2f9c-105">La propriété **DRM \_ keyseed** contient la valeur de départ de clé qui sera utilisée conjointement avec le KeyId pour créer la clé.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a2f9c-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="a2f9c-106">Global Constant</span></span>

<span data-ttu-id="a2f9c-107">g \_ wszWMDRM \_ keyseed</span><span class="sxs-lookup"><span data-stu-id="a2f9c-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="a2f9c-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2f9c-108">Data Type</span></span>

<span data-ttu-id="a2f9c-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a2f9c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2f9c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a2f9c-110">Remarks</span></span>

<span data-ttu-id="a2f9c-111">Cette propriété peut être définie à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="a2f9c-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="a2f9c-112">Elle n’est pas accessible par l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="a2f9c-113">Un Seed de clé est généralement utilisé pour protéger plusieurs fichiers ou ensembles de fichiers, par exemple tous les fichiers émis par un serveur de licences, ou peut-être tous les fichiers par un artiste particulier.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="a2f9c-114">Le KeyID, toutefois, est unique pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="a2f9c-115">La valeur initiale de la clé doit rester un secret partagé uniquement entre le créateur du contenu et le serveur de distribution de licences.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="a2f9c-116">Cette valeur n’est pas stockée dans l’en-tête DRM et n’est ni nécessaire ni accessible aux applications de lecteur DRM.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="a2f9c-117">Une nouvelle valeur initiale de clé peut être générée à l’aide de la méthode [**IWMDRMWriter :: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) ou par tout autre moyen approprié.</span><span class="sxs-lookup"><span data-stu-id="a2f9c-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2f9c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f9c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f9c-119">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="a2f9c-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




