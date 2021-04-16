---
description: Pour compliquer la tâche d’un Interloper pour remplacer une liste de certificats de confiance (CTL) erronée pour une liste existante, vérifiez la signature sur la liste CTL chaque fois que la liste CTL est utilisée.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Vérification d’une liste CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527615"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="c9daf-103">Vérification d’une liste CTL</span><span class="sxs-lookup"><span data-stu-id="c9daf-103">Verifying a CTL</span></span>

<span data-ttu-id="c9daf-104">Pour compliquer la tâche d’un Interloper pour remplacer une liste de [*certificats de confiance*](../secgloss/c-gly.md) (CTL) erronée pour une liste existante, vérifiez la signature sur la liste CTL chaque fois que la liste CTL est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c9daf-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="c9daf-105">N’utilisez pas de liste CTL qui ne contient pas de signature approuvée.</span><span class="sxs-lookup"><span data-stu-id="c9daf-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="c9daf-106">**Pour vérifier une signature CTL**</span><span class="sxs-lookup"><span data-stu-id="c9daf-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="c9daf-107">Ouvrez le [*magasin de certificats*](../secgloss/c-gly.md) contenant la liste de certificats de confiance souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c9daf-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="c9daf-108">Obtient un handle vers un [**\_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) pour la liste CTL.</span><span class="sxs-lookup"><span data-stu-id="c9daf-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="c9daf-109">Pour ce faire, vous pouvez appeler l’une des fonctions qui retournent un handle vers le **\_ contexte** de la liste de certificats de confiance, par exemple [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="c9daf-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="c9daf-110">Appelez [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), en passant [**le \_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la liste de certificats de confiance récupéré à l’étape 2 dans le paramètre *hCryptMsg* , un descripteur du magasin de certificats contenant le certificat de la source approuvée pour les listes CTL dans le paramètre *rghSignerStore* et l' \_ indicateur de signataire approuvé CMSG \_ \_ dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="c9daf-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="c9daf-111">Si la fonction retourne la **valeur true**, la signature a été vérifiée et un pointeur vers le [**\_ contexte PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) du signataire de la liste de certificats de confiance est retourné dans le paramètre *ppSigner* .</span><span class="sxs-lookup"><span data-stu-id="c9daf-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
