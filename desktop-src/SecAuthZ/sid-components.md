---
description: Composants SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Composants SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034083"
---
# <a name="sid-components"></a>Composants SID

Une valeur SID comprend des composants qui fournissent des informations sur la structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) et les composants qui identifient de manière unique un tiers de confiance. Un SID est constitué des composants suivants :

-   Niveau de révision de la structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid)
-   Valeur d’autorité d’identificateur 48 bits qui identifie l’autorité qui a émis le SID
-   Nombre variable de valeurs de sous-autorité ou d' [*identificateur relatif*](/windows/desktop/SecGloss/r-gly) (RID) qui identifient de façon unique le tiers de confiance par rapport à l’autorité qui a émis le SID

La combinaison de la valeur de l’autorité de l’identificateur et des valeurs de la sous-autorité garantit que deux sid ne sont pas les mêmes, même si deux autorités d’émission de SID différentes émettent la même combinaison de valeurs RID. Chaque autorité émettrice de SID émet un RID donné une seule fois.

Les SID sont stockés au format binaire dans une structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) . Pour afficher un SID, vous pouvez appeler la fonction [**ConvertSidToStringSid a**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) pour convertir un SID binaire en format de chaîne. Pour convertir une chaîne SID en un SID fonctionnel valide, appelez la fonction [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .

Ces fonctions utilisent la notation de chaîne standardisée suivante pour les SID, ce qui simplifie la visualisation de leurs composants :

s-*R* - *I* - *s*...

Dans cette notation, le caractère littéral « S » identifie la série de chiffres comme un SID, *R* est le niveau de révision, *I* est l’identificateur-valeur de l’autorité et *S*... est une ou plusieurs valeurs de sous-autorité.

L’exemple suivant utilise cette notation pour afficher le SID relatif au domaine connu du groupe Administrateurs local :

S-1-5-32-544

Dans cet exemple, le SID possède les composants suivants. Les constantes entre parenthèses sont une autorité d’identificateur connue et des valeurs [*RID*](/windows/desktop/SecGloss/r-gly) définies dans Winnt. h :

-   Un niveau de révision de 1
-   Valeur d’autorité d’identificateur 5 (autorité de sécurité \_ NT \_ )
-   La première valeur de sous-autorité 32 ( \_ sécurité \_ BuiltIn \_ RID)
-   Une deuxième valeur de sous-autorité de 544 ( \_ administrateurs RID d’alias de domaine \_ \_ )

 

 
