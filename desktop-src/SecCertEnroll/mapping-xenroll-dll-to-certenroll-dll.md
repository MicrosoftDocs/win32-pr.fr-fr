---
description: La bibliothèque de Xenroll.dll a été supprimée du système d’exploitation et remplacée par CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Mappage de Xenroll.dll à CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8cd2286823dbf8029896c8656807f614dc0e1994fda908cd9b13ec8ad24c7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993528"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Mappage de Xenroll.dll à CertEnroll.dll

avant Windows Vista, le contrôle d’inscription de certificat était implémenté dans Xenroll.dll. La bibliothèque de Xenroll.dll a été supprimée du système d’exploitation et remplacée par CertEnroll.dll.

Xenroll a tenté d’implémenter deux jeux d’interfaces parallèles. [**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)et [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) étaient conformes à Automation et compatibles avec les langages de script. Les interfaces correspondantes ([**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)et [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)) n’ont pas pu être scriptées, mais étaient plus pratiques pour les programmeurs C++. Au fur et à mesure qu’elles ont évolué, les deux jeux d’interfaces n’étaient pas synchronisés. En particulier, l’ensemble des interfaces doubles représentées par **ICEnroll4** ne définit qu’un sous-ensemble des fonctionnalités définies par **IEnroll4**.

CertEnroll.dll implémente un ensemble plus étendu et plus structuré d’interfaces COM conformes à Automation. Les rubriques suivantes expliquent comment Xenroll.dll est mappé à CertEnroll.dll pour différents types de fonctionnalités.

-   [Fonctions de demande de certificat](certificate-request-functions.md)
-   [Fonctions de réponse de certificat](certificate-response-functions.md)
-   [Fonctions d’attribut](attribute-functions.md)
-   [Fonctions d’extension](extension-functions.md)
-   [Fonctions de propriété externes](external-property-functions.md)
-   [Fonctions de clés privées et publiques](private-and-public-key-functions.md)
-   [Fonctions du fournisseur de services de chiffrement](cryptographic-service-provider-functions.md)
-   [Fonctions du magasin de certificats](certificate-store-functions.md)
-   [fonctions d’informations personnelles Exchange](personal-information-exchange-functions.md)
-   [Fonctions d’assistance](helper-functions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
