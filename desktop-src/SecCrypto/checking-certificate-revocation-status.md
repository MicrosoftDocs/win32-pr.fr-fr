---
description: CAPICOM n’active pas la vérification de la révocation des certificats par défaut.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Vérification de l’état de révocation de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204129"
---
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="ed31b-103">Vérification de l’état de révocation de certificat</span><span class="sxs-lookup"><span data-stu-id="ed31b-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="ed31b-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed31b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ed31b-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ed31b-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="ed31b-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="ed31b-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="ed31b-107">CAPICOM n’active pas la vérification de la révocation des certificats par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed31b-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="ed31b-108">Toutefois, la vérification de la révocation des certificats peut être activée par programme pour un certificat particulier via la propriété **IsValid. CheckFlag** d’un objet de certificat.</span><span class="sxs-lookup"><span data-stu-id="ed31b-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="ed31b-109">Une fois la valeur appropriée de **CheckFlag** définie, l’accès à la propriété **IsValid. Result** de l’objet de certificat ou la génération du chemin de vérification du certificat à l’aide de la méthode de génération d’un objet chaîne force la vérification de la révocation.</span><span class="sxs-lookup"><span data-stu-id="ed31b-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="ed31b-110">Dans l’exemple suivant, le certificat a été instancié en tant que certificat CAPICOM valide.</span><span class="sxs-lookup"><span data-stu-id="ed31b-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



<span data-ttu-id="ed31b-111">Le précédent s’applique à un certificat individuel, quelle que soit la façon dont il a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="ed31b-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="ed31b-112">L’exécution de la vérification de la révocation sur les certificats dans un objet [**SignedData**](signeddata.md) n’est pas différente, car la méthode [**verify**](signeddata-verify.md) de l’objet **SignedData** ne peut pas être utilisée à cet effet, car l’activation de la signature et du certificat de CAPICOM \_ \_ \_ \_ ne provoque pas de vérification de la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="ed31b-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="ed31b-113">Au lieu de cela, le **CheckFlag** doit être défini pour chaque certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="ed31b-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="ed31b-114">Prenons l’exemple suivant dans lequel sData a été instancié en tant qu’objet CAPICOM [**SignedData**](signeddata.md) valide.</span><span class="sxs-lookup"><span data-stu-id="ed31b-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



<span data-ttu-id="ed31b-115">L’exemple supplémentaire est la boucle sur tous les certificats de l’objet [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="ed31b-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



