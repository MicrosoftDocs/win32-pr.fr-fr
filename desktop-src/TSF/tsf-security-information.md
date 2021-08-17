---
title: Security Considerations Text Services Framework
description: Security Considerations Text Services Framework
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Text Services Framework (TSF), sécurité
- TSF (Text Services Framework), sécurité
- services de texte, sécurité
- Applications compatibles TSF, sécurité
- sécurité pour TSF
- Text Services Framework (TSF), meilleures pratiques
- TSF (Text Services Framework), meilleures pratiques
- Applications compatibles TSF, meilleures pratiques
- services de texte, meilleures pratiques
- meilleures pratiques pour TSF
- Text Services Framework (TSF), vérification des erreurs
- TSF (Text Services Framework), vérification des erreurs
- Applications compatibles TSF, vérification des erreurs
- services de texte, vérification des erreurs
- vérification des erreurs
- Text Services Framework (TSF), signatures numériques
- TSF (Text Services Framework), signatures numériques
- services de texte, signatures numériques
- Applications compatibles TSF, signatures numériques
- signatures numériques
- Text Services Framework (TSF), LoadLibrary appelle
- TSF (Text Services Framework), LoadLibrary appelle
- services de texte, LoadLibrary appelle
- Applications compatibles TSF, LoadLibrary appelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432418fbcb6221082083d6595aa374939bc2f4d5cf5aad145cac87444e75bdc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873574"
---
# <a name="security-considerations-text-services-framework"></a>Considérations relatives à la sécurité : Text Services Framework

## <a name="best-practices-for-developing-with-tsf"></a>Meilleures pratiques pour le développement avec TSF

-   **Signatures numériques :** Les fournisseurs de services de texte doivent fournir des signatures numériques avec leurs exécutables binaires. Un service de texte inscrit a accès aux threads système et peut exposer des informations qui seraient autrement inaccessibles. Pour garantir un fonctionnement stable et sécurisé, l’utilisateur doit vérifier la signature numérique d’un service de texte avant que le service de texte ne soit autorisé à charger. Consultez [Introduction à la signature du code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) pour connaître la procédure appropriée pour créer une signature numérique.
-   **Vérification des erreurs :** La réussite de chaque appel de méthode ou de fonction doit être vérifiée. En cas d’échec, les appels de méthode ou de fonction restants doivent être ignorés. La plupart des exemples de code de cette documentation ont une vérification limitée des erreurs, ou aucun d’entre eux, pour éviter d’obscurcir le point à illustrer. Vous ne devez pas coller des exemples de la documentation directement dans le code de production ; au lieu de cela, vous devez améliorer les exemples en ajoutant votre propre vérification des erreurs.

-   **LoadLibrary appelle :** Pour obtenir un pointeur vers l’une des [fonctions TSF](text-services-framework-functions.md), vous devrez utiliser [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Toutefois, il est important de suivre les procédures de mise en forme du nom du chemin d’accès à la DLL, comme indiqué dans la documentation de **LoadLibrary** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques de sécurité](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[TSF, fonctions](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 