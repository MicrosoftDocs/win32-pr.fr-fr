---
description: Les services de certificats prennent en charge les demandes de certificat basées sur le \# format PKCS 10 et le format keygen (Netscape). Les services de certificats prennent également en charge \# les demandes de renouvellement PKCS 7 et les demandes CMS (Cryptographic Message Syntax).
ms.assetid: 6321ce99-f5d1-4d72-a062-99cffb543731
title: Demandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c2688d512e36dbb4a4b10740d4da6de651eb64780681eee74859dfbb0e86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900574"
---
# <a name="requests"></a>Demandes

Les services de certificats prennent en charge les [*demandes de certificat*](../secgloss/c-gly.md) basées sur le \# format PKCS 10 et le format keygen (Netscape). Les services de certificats prennent également en charge \# les demandes de renouvellement PKCS 7 et les demandes CMS (Cryptographic Message Syntax).

Les services de certificats fournissent également une interface [ICertRequest](/windows/desktop/api/Certcli/nn-certcli-icertrequest) , qui contient des méthodes pour soumettre une demande de certificat et (si la demande est approuvée) pour recevoir le certificat émis résultant.

Des interfaces supplémentaires liées à la sécurité sont disponibles dans le [contrôle d’inscription de certificats](certificate-enrollment-control.md).

 

 
