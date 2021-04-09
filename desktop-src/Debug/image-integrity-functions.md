---
description: Les fonctions d’intégrité de l’image gèrent l’ensemble des certificats dans un fichier image.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Fonctions d’intégrité de l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033662"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="0d962-103">Fonctions d’intégrité de l’image</span><span class="sxs-lookup"><span data-stu-id="0d962-103">Image Integrity Functions</span></span>

<span data-ttu-id="0d962-104">Les fonctions d’intégrité de l’image gèrent l’ensemble des certificats dans un fichier image.</span><span class="sxs-lookup"><span data-stu-id="0d962-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="0d962-105">Des routines sont fournies pour ajouter, supprimer et interroger des certificats.</span><span class="sxs-lookup"><span data-stu-id="0d962-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="0d962-106">Il existe également une fonction permettant d’obtenir le flux d’octets d’un fichier image requis pour calculer un résumé de message du fichier image.</span><span class="sxs-lookup"><span data-stu-id="0d962-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="0d962-107">Cela est nécessaire pour créer des certificats de signature.</span><span class="sxs-lookup"><span data-stu-id="0d962-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="0d962-108">Chaque certificat dans un fichier a un index qui peut changer à mesure que les certificats sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="0d962-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="0d962-109">De nouveaux certificats sont toujours ajoutés à la fin de la liste des certificats existants.</span><span class="sxs-lookup"><span data-stu-id="0d962-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="0d962-110">Autrement dit, ils reçoivent des index qui sont supérieurs à n’importe quel index en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0d962-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="0d962-111">En général, une application ne doit pas supposer qu’un certificat donné a le même index qu’à la dernière fois qu’elle a été référencée.</span><span class="sxs-lookup"><span data-stu-id="0d962-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="0d962-112">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="0d962-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="0d962-113">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="0d962-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="0d962-114">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="0d962-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="0d962-115">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="0d962-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="0d962-116">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="0d962-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="0d962-117">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="0d962-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="0d962-118">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="0d962-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



