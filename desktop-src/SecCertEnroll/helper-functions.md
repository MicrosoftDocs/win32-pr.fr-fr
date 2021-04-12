---
description: Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Fonctions d’assistance (API d’inscription de certificats)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320074"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="6e604-104">Fonctions d’assistance (API d’inscription de certificats)</span><span class="sxs-lookup"><span data-stu-id="6e604-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="6e604-105">Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="6e604-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="6e604-106">Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="6e604-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="6e604-107">binaryBlobToString</span><span class="sxs-lookup"><span data-stu-id="6e604-107">binaryBlobToString</span></span>

<span data-ttu-id="6e604-108">La fonction [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) dans Xenroll.dll convertit un tableau d’octets en chaîne.</span><span class="sxs-lookup"><span data-stu-id="6e604-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="6e604-109">À l’aide de CertEnroll.dll, vous pouvez appeler la méthode [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) sur l’interface [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="6e604-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="6e604-110">stringToBinaryBlob</span><span class="sxs-lookup"><span data-stu-id="6e604-110">stringToBinaryBlob</span></span>

<span data-ttu-id="6e604-111">La fonction [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) dans Xenroll.dll convertit une chaîne en tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="6e604-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="6e604-112">À l’aide de CertEnroll.dll, vous pouvez appeler la méthode [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) sur l’interface [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="6e604-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e604-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e604-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e604-114">Mappage de Xenroll.dll à CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="6e604-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="6e604-115">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="6e604-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
