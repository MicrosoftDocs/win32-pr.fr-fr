---
description: Les interfaces d’utilisation générales suivantes sont prises en charge par l’API d’inscription de certificats.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces d’assistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534056"
---
# <a name="helper-interfaces"></a><span data-ttu-id="2d57c-103">Interfaces d’assistance</span><span class="sxs-lookup"><span data-stu-id="2d57c-103">Helper Interfaces</span></span>

<span data-ttu-id="2d57c-104">Les interfaces d’utilisation générales suivantes sont prises en charge par l’API d’inscription de certificats.</span><span class="sxs-lookup"><span data-stu-id="2d57c-104">The following general use interfaces are supported by the Certificate Enrollment API.</span></span>



| <span data-ttu-id="2d57c-105">Interface</span><span class="sxs-lookup"><span data-stu-id="2d57c-105">Interface</span></span>                                                                    | <span data-ttu-id="2d57c-106">Description</span><span class="sxs-lookup"><span data-stu-id="2d57c-106">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d57c-107">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="2d57c-107">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | <span data-ttu-id="2d57c-108">Crée une chaîne encodée en Unicode à partir d’un tableau d’octets, crée un tableau d’octets à partir d’une chaîne encodée en Unicode et modifie le type d’encodage Unicode appliqué à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="2d57c-108">Creates a Unicode-encoded string from a byte array, creates a byte array from a Unicode-encoded string, and modifies the type of Unicode encoding applied to a string.</span></span> |
| [<span data-ttu-id="2d57c-109">**ICertificateAttestationChallenge**</span><span class="sxs-lookup"><span data-stu-id="2d57c-109">**ICertificateAttestationChallenge**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | <span data-ttu-id="2d57c-110">Prend en charge les défis liés à l’attestation de certificat.</span><span class="sxs-lookup"><span data-stu-id="2d57c-110">Supports certificate attestation challenges.</span></span>                                                                                                                           |
| [<span data-ttu-id="2d57c-111">**IObjectId**</span><span class="sxs-lookup"><span data-stu-id="2d57c-111">**IObjectId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | <span data-ttu-id="2d57c-112">Représente un identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="2d57c-112">Represents an object identifier.</span></span>                                                                                                                                       |
| [<span data-ttu-id="2d57c-113">**IObjectIds**</span><span class="sxs-lookup"><span data-stu-id="2d57c-113">**IObjectIds**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | <span data-ttu-id="2d57c-114">Gère une collection d’objets [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .</span><span class="sxs-lookup"><span data-stu-id="2d57c-114">Manages a collection of [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) objects.</span></span>                                                                                                        |
| [<span data-ttu-id="2d57c-115">**IX500DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="2d57c-115">**IX500DistinguishedName**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | <span data-ttu-id="2d57c-116">Représente un nom unique X. 500.</span><span class="sxs-lookup"><span data-stu-id="2d57c-116">Represents an X.500 distinguished name.</span></span>                                                                                                                                |
| [<span data-ttu-id="2d57c-117">**IX509EndorsementKey**</span><span class="sxs-lookup"><span data-stu-id="2d57c-117">**IX509EndorsementKey**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | <span data-ttu-id="2d57c-118">Interface de clé de type EK X. 509</span><span class="sxs-lookup"><span data-stu-id="2d57c-118">X.509 Endorsement Key Interface</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2d57c-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d57c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d57c-120">CertEnroll, interfaces</span><span class="sxs-lookup"><span data-stu-id="2d57c-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



