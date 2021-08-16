---
description: Voici les fonctions ImageHlp.
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Fonctions ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2650d80dfb78f346a5fab22e0adfabdfb11c8e626ad3b5ea39930337feaebe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957108"
---
# <a name="imagehlp-functions"></a>Fonctions ImageHlp

Voici les fonctions ImageHlp.

## <a name="image-access"></a>Accès aux images

Les fonctions d’accès à l’image accèdent aux données d’une image exécutable. Les fonctions fournissent un accès de haut niveau à la base d’images et un accès très spécifique aux parties les plus courantes des données d’une image.

<dl>

[**GetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[**GetImageUnusedHeaderBytes**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[**ImageLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[**ImageUnload**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[**MapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[**SetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[**Échec unmapandload**](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a>Intégrité de l’image

Les fonctions d’intégrité de l’image gèrent l’ensemble des certificats dans un fichier image.

<dl>

[**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a>Modification de l’image

Les fonctions de modification d’image vous permettent de modifier l’image exécutable.

<dl>

[**BindImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[**BindImageEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[**CheckSumMappedFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[**MapFileAndCheckSum**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[**ReBaseImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[**ReBaseImage64**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[**SplitSymbols**](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[**StatusRoutine**](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[**TouchFileTimes**](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[**UpdateDebugInfoFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[**UpdateDebugInfoFileEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



