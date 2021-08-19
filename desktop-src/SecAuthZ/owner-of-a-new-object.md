---
description: Un propriétaire d’objets dispose implicitement \_ d’un accès en écriture à l’objet DAC. Cela signifie que le propriétaire peut modifier la liste de contrôle d’accès discrétionnaire des objets (DACL, Discretionary Access Control List) et peut donc contrôler l’accès à l’objet.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Propriétaire d’un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b787603e9225548e4213259866a6658d637bb85e46588f7260322fc2646128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912125"
---
# <a name="owner-of-a-new-object"></a>Propriétaire d’un nouvel objet

Le propriétaire d’un objet dispose implicitement \_ d’un accès en écriture à l’objet de la DAC. Cela signifie que le propriétaire peut modifier la liste de contrôle d’accès discrétionnaire de l’objet (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) et peut donc contrôler l’accès à l’objet.

Le propriétaire d’un nouvel objet est l’identificateur de [*sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du propriétaire par défaut du jeton [*principal*](/windows/desktop/SecGloss/p-gly) ou d' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) du [*processus*](/windows/desktop/SecGloss/p-gly)de création. Pour récupérer ou définir le propriétaire par défaut dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly), appelez la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) avec la structure du [**\_ propriétaire du jeton**](/windows/desktop/api/Winnt/ns-winnt-token_owner) . Le système ne vous permet pas de définir le propriétaire par défaut d’un jeton sur un SID qui n’est pas valide, tel que le SID d’un autre compte d’utilisateur.

un processus avec le \_ privilège SE prendre \_ possession peut se définir comme propriétaire d’un objet. un processus avec le SE \_ privilège de restauration de \_ nom activé ou avec l' \_ accès de propriétaire en écriture à l’objet peut définir tout SID d’utilisateur ou de groupe valide comme propriétaire d’un objet.

 

 
