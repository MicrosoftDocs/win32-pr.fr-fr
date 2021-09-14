---
description: Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Fonctions d’assistance (API d’inscription de certificats)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009027"
---
# <a name="helper-functions-certificate-enrollment-api"></a>Fonctions d’assistance (API d’inscription de certificats)

Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll. Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques.

## <a name="binaryblobtostring"></a>binaryBlobToString

La fonction [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) dans Xenroll.dll convertit un tableau d’octets en chaîne.

À l’aide de CertEnroll.dll, vous pouvez appeler la méthode [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) sur l’interface [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .

## <a name="stringtobinaryblob"></a>stringToBinaryBlob

La fonction [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) dans Xenroll.dll convertit une chaîne en tableau d’octets.

À l’aide de CertEnroll.dll, vous pouvez appeler la méthode [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) sur l’interface [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
