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
# <a name="checking-certificate-revocation-status"></a>Vérification de l’état de révocation de certificat

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

CAPICOM n’active pas la vérification de la révocation des certificats par défaut. Toutefois, la vérification de la révocation des certificats peut être activée par programme pour un certificat particulier via la propriété **IsValid. CheckFlag** d’un objet de certificat. Une fois la valeur appropriée de **CheckFlag** définie, l’accès à la propriété **IsValid. Result** de l’objet de certificat ou la génération du chemin de vérification du certificat à l’aide de la méthode de génération d’un objet chaîne force la vérification de la révocation.

Dans l’exemple suivant, le certificat a été instancié en tant que certificat CAPICOM valide.


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



Le précédent s’applique à un certificat individuel, quelle que soit la façon dont il a été obtenu. L’exécution de la vérification de la révocation sur les certificats dans un objet [**SignedData**](signeddata.md) n’est pas différente, car la méthode [**verify**](signeddata-verify.md) de l’objet **SignedData** ne peut pas être utilisée à cet effet, car l’activation de la signature et du certificat de CAPICOM \_ \_ \_ \_ ne provoque pas de vérification de la liste de révocation de certificats.

Au lieu de cela, le **CheckFlag** doit être défini pour chaque certificat du signataire. Prenons l’exemple suivant dans lequel sData a été instancié en tant qu’objet CAPICOM [**SignedData**](signeddata.md) valide.


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



L’exemple supplémentaire est la boucle sur tous les certificats de l’objet [**SignedData**](signeddata.md) .

 

 



