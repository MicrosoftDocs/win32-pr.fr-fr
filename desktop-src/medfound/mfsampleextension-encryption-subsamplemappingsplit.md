---
description: Définit le mappage de sous-échantillon pour l’exemple indiquant les octets clairs et chiffrés dans les exemples de données.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Attribut MFSampleExtension_Encryption_SubSampleMappingSplit (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527360"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="444e3-103">\_Attribut SubSampleMappingSplit de chiffrement MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="444e3-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="444e3-104">Définit le mappage de sous-échantillon pour l’exemple indiquant les octets clairs et chiffrés dans les exemples de données.</span><span class="sxs-lookup"><span data-stu-id="444e3-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="444e3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="444e3-105">Data type</span></span>

<span data-ttu-id="444e3-106">**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="444e3-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="444e3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="444e3-107">Remarks</span></span>

<span data-ttu-id="444e3-108">L' **objet BLOB** doit contenir un tableau de plages d’octets en tant que DWORDS, où tous les deux DWORD effectuent un ensemble.</span><span class="sxs-lookup"><span data-stu-id="444e3-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="444e3-109">Le premier DWORD de chaque jeu est le nombre d’octets clairs et le deuxième DWORD de l’ensemble est le nombre d’octets chiffrés.</span><span class="sxs-lookup"><span data-stu-id="444e3-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="444e3-110">Notez qu’une paire de 0 n’est pas un ensemble valide (l’une des valeurs peut être 0, mais pas les deux).</span><span class="sxs-lookup"><span data-stu-id="444e3-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="444e3-111">Le tableau de plages d’octets indique les plages à déchiffrer, y compris la possibilité de déchiffrer la totalité de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="444e3-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="444e3-112">Il est recommandé de ne pas définir ce paramètre sur les exemples clairs, bien qu’il soit possible d’obtenir le même résultat en le définissant avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="444e3-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="444e3-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="444e3-113">Examples</span></span>

<span data-ttu-id="444e3-114">L’exemple suivant montre comment définir le \_ chiffrement de MFSampleExtension \_ SubSampleMappingSplit.</span><span class="sxs-lookup"><span data-stu-id="444e3-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="444e3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="444e3-115">Requirements</span></span>



| <span data-ttu-id="444e3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="444e3-116">Requirement</span></span> | <span data-ttu-id="444e3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="444e3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="444e3-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="444e3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="444e3-119">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="444e3-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="444e3-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="444e3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="444e3-121">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="444e3-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="444e3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="444e3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="444e3-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="444e3-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444e3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="444e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444e3-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="444e3-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="444e3-126">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="444e3-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="444e3-127">MFSampleExtension de \_ contenu \_ KeyId</span><span class="sxs-lookup"><span data-stu-id="444e3-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




