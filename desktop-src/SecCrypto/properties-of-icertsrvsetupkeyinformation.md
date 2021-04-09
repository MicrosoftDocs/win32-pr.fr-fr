---
description: Les propriétés suivantes sont définies par l’interface ICertSrvSetupKeyInformation.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Propriétés de ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865454"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="5923b-103">Propriétés de ICertSrvSetupKeyInformation</span><span class="sxs-lookup"><span data-stu-id="5923b-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="5923b-104">Les propriétés suivantes sont définies par l’interface [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .</span><span class="sxs-lookup"><span data-stu-id="5923b-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="5923b-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="5923b-105">Property</span></span>                                                                           | <span data-ttu-id="5923b-106">Description</span><span class="sxs-lookup"><span data-stu-id="5923b-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5923b-107">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="5923b-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="5923b-108">Obtient ou définit le nom utilisé par le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour générer, stocker ou accéder à la clé.</span><span class="sxs-lookup"><span data-stu-id="5923b-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="5923b-109">**Existing**</span><span class="sxs-lookup"><span data-stu-id="5923b-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="5923b-110">Obtient ou définit une valeur qui indique si la clé privée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="5923b-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="5923b-111">**ExistingCACertificate**</span><span class="sxs-lookup"><span data-stu-id="5923b-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="5923b-112">Obtient ou définit la valeur binaire qui a été encodée à l’aide de [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) et qui est la valeur binaire du certificat d’autorité de certification qui correspond à une clé existante.</span><span class="sxs-lookup"><span data-stu-id="5923b-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="5923b-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="5923b-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="5923b-114">Obtient ou définit le nom de l’algorithme de hachage utilisé pour signer ou vérifier le certificat de l’autorité de certification pour la clé.</span><span class="sxs-lookup"><span data-stu-id="5923b-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="5923b-115">**Longueur**</span><span class="sxs-lookup"><span data-stu-id="5923b-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="5923b-116">Obtient ou définit la force de la clé sur l’une des valeurs prises en charge par le fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="5923b-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="5923b-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="5923b-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="5923b-118">Obtient ou définit le nom du fournisseur de services de chiffrement utilisé pour générer ou stocker la clé privée.</span><span class="sxs-lookup"><span data-stu-id="5923b-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
