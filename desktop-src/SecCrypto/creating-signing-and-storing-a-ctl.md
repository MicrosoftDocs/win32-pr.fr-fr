---
description: Créez une liste de certificats de confiance (CTL) signée et enregistrez-la dans un magasin de certificats.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Création, signature et stockage d’une liste de certificats de confiance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513384"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="14502-103">Création, signature et stockage d’une liste de certificats de confiance</span><span class="sxs-lookup"><span data-stu-id="14502-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="14502-104">Les procédures suivantes permettent de créer une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL) signée et de l’enregistrer dans un magasin de [*certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="14502-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="14502-105">**Pour créer et signer une liste de certificats de confiance**</span><span class="sxs-lookup"><span data-stu-id="14502-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="14502-106">Créez un tableau d’éléments à stocker dans la [*liste de certificats de confiance*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="14502-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="14502-107">Dans le cas de certificats approuvés, il doit s’agir des hachages SHA1 ou MD5 des certificats approuvés.</span><span class="sxs-lookup"><span data-stu-id="14502-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="14502-108">Initialisez une structure d' [**\_ informations CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) qui comprend le tableau d’éléments que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="14502-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="14502-109">Initialise une structure [**d' \_ \_ \_ informations de codage signée par CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .</span><span class="sxs-lookup"><span data-stu-id="14502-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="14502-110">Appelez [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span><span class="sxs-lookup"><span data-stu-id="14502-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="14502-111">Cet appel de fonction retourne un pointeur vers une liste de certificats de confiance (au \# format PKCS 7) signée qui contient la liste des éléments créés à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="14502-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="14502-112">**Pour ajouter une liste CTL à un magasin de certificats**</span><span class="sxs-lookup"><span data-stu-id="14502-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="14502-113">Obtient un pointeur vers une liste de certificats de confiance (CTL) signée et encodée.</span><span class="sxs-lookup"><span data-stu-id="14502-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="14502-114">Ouvrez le magasin de certificats cible avec un appel à [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="14502-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="14502-115">Appelez [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span><span class="sxs-lookup"><span data-stu-id="14502-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
