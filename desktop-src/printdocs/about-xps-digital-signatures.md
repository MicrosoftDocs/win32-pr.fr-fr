---
description: Cette section fournit une vue d’ensemble de l’API de signature numérique XPS.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: À propos de l’API de signature numérique XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115486"
---
# <a name="about-xps-digital-signature-api"></a>À propos de l’API de signature numérique XPS

Les documents XPS peuvent avoir des signatures numériques pour permettre aux utilisateurs de signer un document, vérifier l’identité du signataire et indiquer si un document XPS a été modifié depuis sa signature. Une application Windows Native peut utiliser les interfaces de l’API de signature numérique XPS pour effectuer des opérations de signature numérique sur un document XPS. Cette section fournit une vue d’ensemble de l’API de signature numérique XPS.

L’interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) gère les opérations de signature numérique sur un document XPS. Pour qu’une application puisse accéder aux signatures numériques d’un document XPS, l’application doit appeler [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un **IXpsSignatureManager** , puis appeler [**IXpsSignatureManager :: LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**IXpsSignatureManager :: LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) pour charger le document XPS. Pour plus d’informations sur ce processus d’initialisation, consultez [initialiser le gestionnaire de signatures](initialize-the-signature-manager.md).

Une fois qu’un document XPS a été chargé dans une interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) , une application peut alors accéder aux signatures numériques et aux demandes de signature numérique du document. Vous pouvez accéder aux signatures numériques à l’aide d’une interface [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) à partir de l’interface [**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) du gestionnaire de signature. Une application peut également ajouter et supprimer des interfaces **IXpsSignature** à partir de la collection. Les demandes de signature sont accessibles à l’aide de [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) collectées dans une interface [**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) . **IXpsSignatureRequestCollection** fait partie d’une interface [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) qui sont collectées dans le [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) du gestionnaire de signature.

Les applications peuvent utiliser le [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) du gestionnaire de signatures pour accéder aux options de signature numérique et les définir.

Pour obtenir des exemples d’accès aux signatures numériques d’un document XPS, consultez [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API de signature numérique XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Informations de référence sur l’API de signature numérique XPS](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Standard ECMA-376, formats de fichier Office Open XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
