---
description: Fournit un mécanisme permettant de contrôler l’accès aux objets sécurisables.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: Contrôle d'intégrité par mandat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1a39cfc1d1ab819181e37c17328d6015a884f9ae1cce546643480351341b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781492"
---
# <a name="mandatory-integrity-control"></a>Contrôle d'intégrité par mandat

Contrôle d’intégrité par mandat (MIC) fournit un mécanisme permettant de contrôler l’accès aux objets sécurisables. Ce mécanisme s’ajoute au contrôle d’accès discrétionnaire et évalue l’accès avant l’évaluation des vérifications d’accès par rapport à la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet.

MIC utilise des niveaux d’intégrité et une stratégie obligatoire pour évaluer l’accès. Les [*principaux de sécurité*](/windows/desktop/SecGloss/s-gly) et les objets sécurisables se voient affecter des niveaux d’intégrité qui déterminent leurs niveaux de protection ou d’accès. Par exemple, un principal avec un niveau d’intégrité faible ne peut pas écrire dans un objet avec un niveau d’intégrité moyen, même si la liste DACL de cet objet autorise l’accès en écriture au principal.

Windows définit quatre niveaux d’intégrité : faible, moyen, élevé et système. Les utilisateurs standard reçoivent un support de réception élevé. Les processus que vous démarrez et les objets que vous créez reçoivent votre niveau d’intégrité (moyen ou élevé) ou faible si le niveau du fichier exécutable est faible ; les services système reçoivent l’intégrité du système. Les objets qui n’ont pas d’étiquette d’intégrité sont traités comme moyens par le système d’exploitation ; Cela empêche le code de faible intégrité de modifier des objets sans étiquette. en outre, Windows garantit que les processus exécutés avec un niveau d’intégrité faible ne peuvent pas obtenir l’accès à un processus associé à un conteneur d’application.

## <a name="integrity-labels"></a>Étiquettes d’intégrité

Les étiquettes d’intégrité spécifient les niveaux d’intégrité des objets sécurisables et des principaux de sécurité. Les étiquettes d’intégrité sont représentées par des [*SID d’intégrité*](/windows/desktop/SecGloss/i-gly). Le SID d’intégrité d’un objet sécurisable est stocké dans sa [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). La liste SACL contient une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) [**\_ \_ \_ ACE System Mandatory**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) qui, à son tour, contient le SID d’intégrité. Tout objet sans SID d’intégrité est traité comme s’il avait une intégrité moyenne.

Le SID d’intégrité d’un principal de sécurité est stocké dans son jeton d’accès. Un jeton d’accès peut contenir un ou plusieurs SID d’intégrité.

Pour plus d’informations sur les SID d’intégrité définis, consultez [sid connus](well-known-sids.md).

## <a name="process-creation"></a>Création de processus

Lorsqu’un utilisateur tente de lancer un fichier exécutable, le nouveau processus est créé avec au minimum le niveau d’intégrité de l’utilisateur et le niveau d’intégrité du fichier. Cela signifie que le nouveau processus ne s’exécutera jamais avec une intégrité plus élevée que le fichier exécutable. Si l’utilisateur administrateur exécute un programme à faible intégrité, le jeton pour le nouveau processus fonctionne avec le niveau d’intégrité faible. Cela permet de protéger un utilisateur qui lance du code non fiable à partir d’actes malveillants effectués par ce code. Les données utilisateur, qui sont au niveau d’intégrité utilisateur standard, sont protégées en écriture contre ce nouveau processus.

## <a name="mandatory-policy"></a>Stratégie obligatoire

L’ACE du [**\_ \_ Label \_ obligatoire du système**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) dans la liste SACL d’un objet sécurisable contient un masque d’accès qui spécifie l’accès aux principaux dont les niveaux d’intégrité sont inférieurs à ceux de l’objet. Les valeurs définies pour ce masque d’accès **sont \_ étiquette obligatoire système \_ \_ non \_ écriture \_ vers le haut**, **\_ étiquette système obligatoire \_ \_ non \_ en lecture \_** et **\_ étiquette obligatoire système \_ \_ non \_ exécutée \_**. Par défaut, le système crée chaque objet avec un masque d’accès de l' **\_ étiquette obligatoire système \_ \_ non \_ écrit \_**.

Chaque jeton d’accès spécifie également une stratégie obligatoire qui est définie par l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) lors de la création du jeton. Cette stratégie est spécifiée par une structure de [**\_ \_ stratégie de jeton obligatoire**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) associée au jeton. Cette structure peut être interrogée en appelant la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) avec la valeur du paramètre *TokenInformationClass* défini sur **TokenMandatoryPolicy**.

 

 
