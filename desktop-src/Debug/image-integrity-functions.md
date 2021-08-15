---
description: Les fonctions d’intégrité de l’image gèrent l’ensemble des certificats dans un fichier image.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Fonctions d’intégrité de l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a2311ccfc59fb228a8f71c380205dc754452ba4a9d0a7e1dcb3c9edcd92a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957098"
---
# <a name="image-integrity-functions"></a>Fonctions d’intégrité de l’image

Les fonctions d’intégrité de l’image gèrent l’ensemble des certificats dans un fichier image. Des routines sont fournies pour ajouter, supprimer et interroger des certificats. Il existe également une fonction permettant d’obtenir le flux d’octets d’un fichier image requis pour calculer un résumé de message du fichier image. Cela est nécessaire pour créer des certificats de signature.

Chaque certificat dans un fichier a un index qui peut changer à mesure que les certificats sont supprimés. De nouveaux certificats sont toujours ajoutés à la fin de la liste des certificats existants. Autrement dit, ils reçoivent des index qui sont supérieurs à n’importe quel index en cours d’utilisation. En général, une application ne doit pas supposer qu’un certificat donné a le même index qu’à la dernière fois qu’elle a été référencée.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



