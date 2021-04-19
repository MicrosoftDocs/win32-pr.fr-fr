---
description: La stratégie de ticket Kerberos est définie au niveau du domaine et implémentée par le centre de distribution de clés du domaine (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Stratégie Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531989"
---
# <a name="kerberos-policy"></a>Stratégie Kerberos

La stratégie de ticket Kerberos est définie au niveau du domaine et implémentée par le [*Centre de distribution de clés*](../secgloss/k-gly.md) du domaine (KDC). La stratégie Kerberos est stockée dans le Active Directory en tant que sous-ensemble des attributs de la stratégie de sécurité du domaine. Par défaut, les options de stratégie peuvent être définies uniquement par les membres du groupe administrateurs de domaine. La stratégie de domaine comprend des options qui :

-   Prise en charge des tickets postdatés
-   Prendre en charge la délégation avec restriction (Windows Server 2003 uniquement)
-   Tickets de support qui peuvent être transférés
-   Prendre en charge les tickets renouvelés
-   Définir l’âge maximal du ticket
-   Définir l’âge de renouvellement maximal
-   Définir l’âge maximal du ticket proxy
-   Déconnecter de force les utilisateurs lorsque les tickets expirent

Avec la [*délégation avec restriction*](../secgloss/c-gly.md), un ordinateur peut être configuré pour autoriser le transfert des informations d’identification uniquement vers une liste spécifique de services. Ces services doivent se trouver dans le même domaine que l’ordinateur qui transfère les informations d’identification. Sous la *délégation avec restriction*, les tickets ne sont plus envoyés du client au serveur. L’ordinateur serveur crée des tickets de service pour transférer les informations utilisées pour authentifier le client, le cas échéant.

Bien que la stratégie Kerberos pour un domaine puisse autoriser l’authentification déléguée en autorisant le transfert de tickets, cet aspect de la stratégie ne doit pas s’appliquer à tous les utilisateurs ou à tous les ordinateurs. Un attribut d’un compte d’utilisateur individuel peut être défini pour désactiver le transfert des [*informations d’identification*](../secgloss/c-gly.md) de cet utilisateur par n’importe quel serveur. Un attribut du compte d’un ordinateur individuel peut être défini pour désactiver le transfert des informations d’identification de n’importe quel utilisateur. Dans les deux cas, la délégation peut être désactivée en créant une stratégie de groupe à appliquer à tous les utilisateurs ou à tous les ordinateurs d’une unité d’organisation du Active Directory.

**Windows XP/2000 :** La délégation avec restriction n’est pas prise en charge.

 

 
