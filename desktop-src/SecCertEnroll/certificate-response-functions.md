---
description: Implémente l’interface IX509Enrollment.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Fonctions de réponse de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f82922ce2b0cdfad370bbfbf4d1fd3a135c19d5ba613110364f7283ec12a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902399"
---
# <a name="certificate-response-functions"></a>Fonctions de réponse de certificat

CertEnroll.dll implémente l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour envoyer une demande de certificat client et installer la réponse à partir d’une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) (ca).

Le processus d’inscription peut prendre en charge les trois scénarios suivants :

<dl> Inscription hors-bande

1.  Appelez une méthode d’initialisation implémentée par l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Appelez la méthode [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) pour récupérer la requête.
3.  Envoyez la demande hors bande (manuellement ou à l’aide d’un autre processus).
4.  Recevoir la réponse d’une autorité de certification.
5.  Appelez la méthode [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

  
Inscription automatique

1.  Appelez une méthode d’initialisation implémentée par l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Appelez la méthode d' [**inscription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) .

  
Inscription différée

1.  Appelez une méthode d’initialisation implémentée par l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Appelez la méthode [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) pour récupérer la requête.
3.  Stockez la demande jusqu’à ce que vous soyez prêt à la soumettre.
4.  Lorsque vous êtes prêt à procéder à l’inscription, appelez la méthode [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) pour réinitialiser l’objet d’inscription.
5.  Appelez la méthode [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) lorsque l’autorité de certification retourne un certificat.

  
</dl>

Pendant le processus d’inscription, vous pouvez appeler la propriété [**Status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) sur l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour récupérer une valeur d’énumération [**EnrollmentEnrollStatus**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) qui identifie si l’inscription a réussi, si elle est en attente, si elle a été ignorée, a généré une erreur ou si a été refusé.

Chacune des sections suivantes identifie une fonction exportée par Xenroll.dll pour installer une réponse de certificat à partir d’une autorité de certification. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [acceptFileResponseWStr](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [acceptResponseBlob](#acceptresponseblob)
-   [getCertContextFromFileResponseWStr](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [getCertContextFromResponseBlob](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [SPCFileNameWStr](#spcfilenamewstr)
-   [WriteCertToCSP](#writecerttocsp)
-   [WriteCertToUserDS](#writecerttouserds)
-   [Rubriques connexes](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

La fonction [**acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) dans Xenroll.dll installe une réponse [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) à partir d’un fichier.

La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités pour installer une \# réponse de certificat PKCS 7 à partir d’un fichier. Toutefois, vous pouvez créer une fonction personnalisée pour lire les données de fichier dans un tableau d’octets et appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer la réponse.

Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat fictif n’a pas besoin d’exister, ce qui vous permet d’installer un certificat sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="acceptfileresponsewstr"></a>acceptFileResponseWStr

La fonction [**acceptFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) dans Xenroll.dll installe une \# réponse de certificat PKCS 7 ou CMC à partir d’un fichier.

La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités pour installer une réponse de certificat à partir d’un fichier. Toutefois, vous pouvez créer une fonction personnalisée pour lire les données de fichier dans un tableau d’octets et appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer la \# réponse PKCS 7 ou CMC.

Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat fictif n’a pas besoin d’exister, ce qui vous permet d’installer un certificat sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

La fonction [**acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) dans Xenroll.dll installe une \# réponse PKCS 7 contenue dans un tableau d’octets.

Vous pouvez appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer un \# message PKCS 7. Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat fictif n’a pas besoin d’exister, ce qui vous permet d’installer la \# réponse PKCS 7 sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="acceptresponseblob"></a>acceptResponseBlob

La fonction [**acceptResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) dans Xenroll.dll installe une \# réponse de certificat PKCS 7 ou CMC contenue dans un tableau d’octets.

Vous pouvez appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer une \# réponse PKCS 7 ou CMC. Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat factice n’a pas besoin d’exister, ce qui vous permet d’installer la réponse sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="getcertcontextfromfileresponsewstr"></a>getCertContextFromFileResponseWStr

La fonction [**getCertContextFromFileResponseWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) dans Xenroll.dll récupère le certificat client à partir d’un fichier.

La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités permettant de récupérer un certificat à partir d’une réponse de l’autorité de certification enregistrée dans un fichier. Toutefois, vous pouvez créer une fonction personnalisée pour lire les données de fichier dans un tableau d’octets et appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer la \# réponse PKCS 7 ou CMC, et appeler la propriété [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) pour récupérer le certificat.

Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat fictif n’a pas besoin d’exister, ce qui vous permet d’installer un certificat sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

La fonction [**getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) dans Xenroll.dll récupère le certificat client à partir d’une \# réponse PKCS 7.

Vous pouvez appeler la propriété [**certificat**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) sur l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour récupérer un certificat après avoir appelé la méthode [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

## <a name="getcertcontextfromresponseblob"></a>getCertContextFromResponseBlob

La fonction [**getCertContextFromResponseBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) dans Xenroll.dll récupère un certificat client à partir d’une \# réponse PKCS 7 ou CMC.

Vous pouvez appeler la propriété [**certificat**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) sur l’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour récupérer un certificat après avoir appelé la méthode [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

La fonction [**InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) dans Xenroll.dll installe une \# réponse PKCS 7.

Vous pouvez appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer une \# réponse PKCS 7 ou CMC. Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat factice n’a pas besoin d’exister, ce qui vous permet d’installer la réponse sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

La fonction [**InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) dans Xenroll.dll installe une \# réponse PKCS 7 et retourne le nombre de certificats installés.

Vous pouvez appeler [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) pour installer une \# réponse PKCS 7 ou CMC. Si vous spécifiez la valeur **AllowNoOutstandingRequest** de l’énumération [**InstallResponseRestrictionFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) pour le premier paramètre de [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), un certificat factice n’a pas besoin d’exister, ce qui vous permet d’installer la réponse sans appeler d’abord [**ENROLL**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) ou [**CreateRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Toutefois, si vous installez un certificat à l’aide d’un script Web, un certificat factice doit exister dans le magasin de demandes. Vous devez donc spécifier **AllowNone** pour le premier paramètre.

## <a name="spcfilenamewstr"></a>SPCFileNameWStr

La fonction [**SPCFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) dans Xenroll.dll spécifie ou récupère le nom du fichier dans lequel enregistrer la réponse du certificat. La bibliothèque CertEnroll.dll n’implémente pas les fonctionnalités qui vous permettent de copier un certificat dans un fichier spécifique. Le processus d’inscription installe automatiquement la chaîne de certificats dans des fichiers dans les magasins appropriés.

## <a name="writecerttocsp"></a>WriteCertToCSP

La fonction [**WriteCertToCSP**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique si un certificat doit être écrit dans un [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP). En général, si cette fonction est appelée, le fournisseur est une [*carte à puce*](/windows/desktop/SecGloss/s-gly).

Dans CertEnroll.dll, lorsqu’un client appelle la méthode d' [**inscription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) pour soumettre une demande de certificat de carte à puce et qu’un certificat est émis, l' [**inscription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) installe automatiquement le certificat sur la carte à puce en supposant que la carte est installée dans le lecteur. La méthode [**InstallResponse**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) écrit également automatiquement le certificat sur la carte à puce.

## <a name="writecerttouserds"></a>WriteCertToUserDS

La fonction [**WriteCertToUserDS**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique si un certificat doit être enregistré dans le magasin de Active Directory. La bibliothèque CertEnroll.dll n’implémente pas les fonctionnalités qui vous permettent de spécifier un magasin vers lequel copier un certificat.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
