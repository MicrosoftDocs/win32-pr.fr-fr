---
description: La plupart des fonctions requièrent des types d’encodage de message ou de certificat.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Types d’encodage de message et de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484696"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="75726-103">Types d’encodage de message et de certificat</span><span class="sxs-lookup"><span data-stu-id="75726-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="75726-104">La plupart des fonctions requièrent des [*types d’encodage de message*](../secgloss/m-gly.md)ou de certificat.</span><span class="sxs-lookup"><span data-stu-id="75726-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="75726-105">Ce type d’encodage est une **valeur DWORD** qui contient éventuellement le certificat et les types d’encodage de message.</span><span class="sxs-lookup"><span data-stu-id="75726-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="75726-106">Le type d’encodage de certificat est stocké dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="75726-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="75726-107">Le type d’encodage de message est stocké dans le mot de poids fort.</span><span class="sxs-lookup"><span data-stu-id="75726-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="75726-108">Certains champs de fonction ou de structure nécessitent uniquement l’un des types d’encodage, mais il est toujours acceptable de spécifier les deux types d’encodage.</span><span class="sxs-lookup"><span data-stu-id="75726-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="75726-109">Pour obtenir un exemple de spécification des deux types d’encodage, consultez [ \# includes et \# definis](-includes-and--defines.md).</span><span class="sxs-lookup"><span data-stu-id="75726-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="75726-110">La Convention d’affectation de noms de paramètres suivante est utilisée pour indiquer les types d’encodage requis.</span><span class="sxs-lookup"><span data-stu-id="75726-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="75726-111">Nom</span><span class="sxs-lookup"><span data-stu-id="75726-111">Name</span></span>                       | <span data-ttu-id="75726-112">Commentaires</span><span class="sxs-lookup"><span data-stu-id="75726-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75726-113">*dwMsgAndCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="75726-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="75726-114">Les deux types d’encodage sont requis.</span><span class="sxs-lookup"><span data-stu-id="75726-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="75726-115">*dwMsgEncodingType*</span><span class="sxs-lookup"><span data-stu-id="75726-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="75726-116">Seul le type d’encodage de message est requis.</span><span class="sxs-lookup"><span data-stu-id="75726-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="75726-117">*dwCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="75726-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="75726-118">Seul le type d’encodage de certificat est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="75726-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="75726-119">*dwEncodingType*</span><span class="sxs-lookup"><span data-stu-id="75726-119">*dwEncodingType*</span></span>           | <span data-ttu-id="75726-120">Un message ou un type d’encodage de certificat est requis.</span><span class="sxs-lookup"><span data-stu-id="75726-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="75726-121">Si le mot de poids faible contenant le type d’encodage de certificat est différent de zéro, il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="75726-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="75726-122">Dans le cas contraire, le mot de poids fort contenant le type d’encodage de message est utilisé.</span><span class="sxs-lookup"><span data-stu-id="75726-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="75726-123">Si les deux sont spécifiés, le type d’encodage de certificat dans le mot de poids faible est utilisé.</span><span class="sxs-lookup"><span data-stu-id="75726-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="75726-124">Les types d’encodage actuellement définis sont présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="75726-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="75726-125">Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="75726-125">Encoding type</span></span>          | <span data-ttu-id="75726-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="75726-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="75726-127">CRYPTer l' \_ \_ encodage ASN</span><span class="sxs-lookup"><span data-stu-id="75726-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="75726-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="75726-128">0x00000001</span></span> |
| <span data-ttu-id="75726-129">\_Codage ASN \_ x509</span><span class="sxs-lookup"><span data-stu-id="75726-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="75726-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="75726-130">0x00000001</span></span> |
| <span data-ttu-id="75726-131">Encodage ASN de PKCS \_ 7 \_ \_</span><span class="sxs-lookup"><span data-stu-id="75726-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="75726-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="75726-132">0x00010000</span></span> |



 

 

 
