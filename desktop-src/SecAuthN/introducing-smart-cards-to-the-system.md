---
description: Pour que le sous-système de carte à puce puisse trouver une carte à puce, la carte à puce doit être introduite sur le système.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Présentation des cartes à puce au système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210014"
---
# <a name="introducing-smart-cards-to-the-system"></a>Présentation des cartes à puce au système

Pour que le [*sous-système de carte à*](../secgloss/s-gly.md) puce puisse trouver une [*carte*](../secgloss/s-gly.md)à puce, la carte à puce doit être introduite sur le système. Cette opération est généralement effectuée à l’aide d’un outil de configuration de carte à puce fourni par le fabricant de la carte. L’outil peut être un programme sur une disquette (avec la carte à puce), un contrôle ActiveX disponible sur un site Web, et ainsi de suite.

L’outil d’installation doit fournir les informations suivantes sur la carte :

-   Sa [*chaîne ATR*](../secgloss/a-gly.md)et un masque facultatif à utiliser comme aide pour identifier la carte.
-   Liste des interfaces de carte à puce prises en charge par la carte.
-   Nom complet de la carte, à utiliser pour identifier la carte à l’utilisateur. Dans la plupart des cas, l’utilisateur le fournira à l’outil d’installation.
-   [*Fournisseur de services principal*](../secgloss/p-gly.md) associé à la carte (facultatif) à utiliser lors de l’accès à la carte via des interfaces com.

Pour simplifier les outils d’installation et garantir l’intégrité de la [*base de données des cartes à puce*](../secgloss/s-gly.md), le sous-système de carte à puce fournit les deux fonctions suivantes. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduit une carte à puce dans la base de données et [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) le supprime de la base de données.

 

 
