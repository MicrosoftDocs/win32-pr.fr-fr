---
description: Les extensions sont incluses dans une \# demande de certificat PKCS 10 en les ajoutant au champ attributs de la structure CertificationRequestInfo présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations, consultez la rubrique attributs.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: '\#Extensions PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531197"
---
# <a name="pkcs-10-extensions"></a><span data-ttu-id="4f057-104">\#Extensions PKCS 10</span><span class="sxs-lookup"><span data-stu-id="4f057-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="4f057-105">Les extensions sont incluses dans une \# demande de certificat PKCS 10 en les ajoutant au champ **attributs** de la structure **CertificationRequestInfo** présentée dans l’exemple de Syntaxe ASN. 1 suivant.</span><span class="sxs-lookup"><span data-stu-id="4f057-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="4f057-106">Pour plus d’informations, consultez la rubrique [attributs](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4f057-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="4f057-107">La procédure suivante explique comment utiliser l’API d’inscription de certificats pour ajouter des extensions à une demande de \# certificat PKCS 10 :</span><span class="sxs-lookup"><span data-stu-id="4f057-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="4f057-108">Récupérez une collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en appelant la propriété [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) sur l’objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="4f057-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="4f057-109">Créez une extension en utilisant l’une des interfaces disponibles qui dérivent de l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="4f057-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="4f057-110">Ajoutez les extensions créées à l’étape 2 à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) Récupérée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="4f057-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f057-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f057-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f057-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="4f057-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="4f057-113">Architecture des attributs</span><span class="sxs-lookup"><span data-stu-id="4f057-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="4f057-114">\#Attributs PKCS 10</span><span class="sxs-lookup"><span data-stu-id="4f057-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f057-115">Extensions</span><span class="sxs-lookup"><span data-stu-id="4f057-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



