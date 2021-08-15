---
description: En plus des certificats et des listes de révocation de certificats (CRL), le magasin de certificats CryptoAPI prend en charge la liste de certificats de confiance (CTL).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Présentation de la liste de certificats de confiance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7906f02e9af3534445c5b1d6a48c94653feb78b57c71a23acfd9af51477cd050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771105"
---
# <a name="certificate-trust-list-overview"></a>Présentation de la liste de certificats de confiance

En plus des certificats et des [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL), le magasin de [*certificats*](../secgloss/c-gly.md) [*CryptoAPI*](../secgloss/c-gly.md) prend en charge la liste de certificats de [*confiance*](../secgloss/c-gly.md) (CTL). Une liste CTL est une liste prédéfinie d’éléments signés par une entité approuvée. Une liste de certificats de confiance est une liste de [*hachages*](../secgloss/h-gly.md) de certificats ou une liste de noms de fichiers. Tous les éléments de la liste sont authentifiés et approuvés par une entité de signature approuvée. Une structure de [**\_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) est similaire aux structures de contexte de certificat et de liste de révocation de certificats. Un contexte de liste de certificats de confiance peut être conservé dans le magasin de certificats.

Une CTL CryptoAPI est une liste d’éléments qui ont été signés par une entité approuvée. La liste des éléments peut être n’importe quel élément, par exemple une liste de hachages de certificats ou une liste de noms de fichiers. Dans la plupart des cas, une liste CTL est une liste de contextes de certificat hachés. Tous les éléments de la liste sont authentifiés et approuvés par l’entité de signature. L’utilisation principale des listes CTL consiste à vérifier les messages signés, en utilisant la liste CTL comme source de [*certificats racines*](../secgloss/r-gly.md)approuvés.

La structure du contexte de la liste de certificats de [**confiance \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) est similaire aux structures de contexte du certificat et de la liste de révocation des certificats ; Toutefois, contrairement aux **structures de** contexte du certificat et **de la liste \_** de révocation de certificats Ce handle est ouvert par un appel à l’une des fonctions qui retournent une structure de **\_ contexte CTL** , ce qui permet d’utiliser les fonctions de message pour vérifier la signature de la liste de certificats de confiance. Cette vérification est nécessaire pour s’assurer qu’une liste CTL n’est pas une liste de certificats de confiance qui n’est pas complantée par une entité non autorisée.

Pour connaître les procédures de création d’une liste CTL signée et de l’enregistrer dans un magasin de certificats, consultez [création, signature et stockage d’une liste CTL](creating-signing-and-storing-a-ctl.md). Consultez également [vérification d’une liste de certificats de confiance](verifying-a-ctl.md) et [vérification des messages signés à l’aide de listes CTL](verifying-signed-messages-by-using-ctls.md) pour les procédures de vérification pas à pas.

 

 
