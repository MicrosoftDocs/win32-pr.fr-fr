---
title: DRM_HeaderSignPrivKey
description: La \_ propriété DRM HeaderSignPrivKey contient la clé privée utilisée pour signer l’en-tête ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- Format Windows Media DRM_HeaderSignPrivKey
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723490"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="2bfce-104">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="2bfce-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="2bfce-105">La propriété **DRM \_ HeaderSignPrivKey** contient la clé privée utilisée pour signer l’en-tête ASF.</span><span class="sxs-lookup"><span data-stu-id="2bfce-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="2bfce-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="2bfce-106">Global Constant</span></span>

<span data-ttu-id="2bfce-107">g \_ wszWMDRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="2bfce-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="2bfce-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="2bfce-108">Data Type</span></span>

<span data-ttu-id="2bfce-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="2bfce-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="2bfce-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2bfce-110">Remarks</span></span>

<span data-ttu-id="2bfce-111">Cette propriété est générée à l’aide de [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span><span class="sxs-lookup"><span data-stu-id="2bfce-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="2bfce-112">Conservez ce secret clé et partagez la clé publique uniquement avec le service de licence.</span><span class="sxs-lookup"><span data-stu-id="2bfce-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="2bfce-113">Une fois que vous avez défini cette clé, le composant DRM l’utilise pour signer l’en-tête de fichier ASF (pas l’en-tête DRM qui est signé avec les valeurs d’objet de signature numérique comme DRM \_ LASignaturePrivKey).</span><span class="sxs-lookup"><span data-stu-id="2bfce-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="2bfce-114">Évidemment, **DRM \_ HeaderSignPrivKey** n’est pas inclus dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="2bfce-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="2bfce-115">Cette propriété n’est pas accessible à partir de l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="2bfce-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="2bfce-116">Il peut être défini à partir de l’objet Writer à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="2bfce-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="2bfce-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bfce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bfce-118">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="2bfce-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




