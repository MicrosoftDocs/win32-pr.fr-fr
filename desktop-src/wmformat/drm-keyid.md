---
title: DRM_KeyID
description: L' \_ attribut DRM KeyId contient l’identificateur de clé.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- Format Windows Media DRM_KeyID
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030836"
---
# <a name="drm_keyid"></a><span data-ttu-id="90849-104">\_KEYID DRM</span><span class="sxs-lookup"><span data-stu-id="90849-104">DRM\_KeyID</span></span>

<span data-ttu-id="90849-105">L’attribut **DRM \_ KeyId** contient l’identificateur de clé.</span><span class="sxs-lookup"><span data-stu-id="90849-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="90849-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="90849-106">Global Constant</span></span>

<span data-ttu-id="90849-107">g \_ wszWMDRM \_ KeyId</span><span class="sxs-lookup"><span data-stu-id="90849-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="90849-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="90849-108">Data Type</span></span>

<span data-ttu-id="90849-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="90849-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="90849-110">Notes</span><span class="sxs-lookup"><span data-stu-id="90849-110">Remarks</span></span>

<span data-ttu-id="90849-111">Cet attribut est présent uniquement pour le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="90849-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="90849-112">Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="90849-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="90849-113">Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ KeyId**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="90849-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="90849-114">L’ID de clé est utilisé conjointement avec la valeur initiale de la clé pour créer la clé de contenu qui est utilisée pour chiffrer et déchiffrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="90849-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="90849-115">L’application Writer utilise l’ID de clé pour chiffrer le fichier, puis stocke l’ID de clé dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="90849-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="90849-116">Quand une application de lecteur demande une licence pour un fichier, le composant DRM envoie l’ID de clé (ainsi que le reste de l’en-tête DRM) au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="90849-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="90849-117">Le serveur de licences, qui a la valeur initiale de clé secrète, l’utilise et l’ID de clé pour créer une clé pour le fichier, qu’il insère ensuite dans une licence avec les différents droits qui seront appliqués au fichier.</span><span class="sxs-lookup"><span data-stu-id="90849-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="90849-118">En règle générale, une valeur initiale de clé est utilisée avec de nombreux ID de clé.</span><span class="sxs-lookup"><span data-stu-id="90849-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="90849-119">L’amorce de clé est un secret partagé uniquement par le créateur de contenu et le serveur de distribution de licences.</span><span class="sxs-lookup"><span data-stu-id="90849-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="90849-120">L’ID de clé est utilisé par les applications clientes DRM et est stocké dans l’en-tête DRM en clair.</span><span class="sxs-lookup"><span data-stu-id="90849-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="90849-121">Cet attribut est identique à [**DRM \_ DRMHeader \_ KeyId**](drm-drmheader-keyid.md).</span><span class="sxs-lookup"><span data-stu-id="90849-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="90849-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90849-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90849-123">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="90849-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




