---
title: Fonctions de service d’annuaire (gestion de réseau)
description: Les fonctions de service d’annuaire de gestion de réseau permettent aux développeurs de travailler avec le contrôleur de domaine et l’appartenance au domaine dans le service d’annuaire.
ms.assetid: 9eeb8f40-85c0-49db-a307-193703e4f463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e843e06762b4a7ef55b3f979b12a62ee6adf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009418"
---
# <a name="directory-service-functions"></a>Fonctions du service d’annuaire

Les fonctions de service d’annuaire de gestion de réseau permettent aux développeurs de travailler avec le contrôleur de domaine et l’appartenance au domaine dans le service d’annuaire.

Les fonctions du service d’annuaire de gestion de réseau sont répertoriées ci-dessous.



| Fonction                                                                 | Description                                                                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)       | Ajoute un autre nom pour l’ordinateur spécifié.                                                                                                                                          |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)           | Énumère les noms de l’ordinateur spécifié.                                                                                                                                                |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                           | Récupère une liste d’unités d’organisation dans laquelle un compte d’ordinateur peut être créé.                                                                                                  |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                   | Récupère les informations sur l’état de la jointure pour l’ordinateur spécifié.                                                                                                                               |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                   | Joint un ordinateur à un groupe de travail ou à un domaine.                                                                                                                                                  |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)       | Provisionne un compte d’ordinateur pour une utilisation ultérieure dans une opération de jonction de domaine hors connexion.                                                                                                           |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername) | Supprime un autre nom pour l’ordinateur spécifié.                                                                                                                                       |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)             | Modifie le nom d’un ordinateur dans un domaine.                                                                                                                                                 |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)           | Définit le nom de l’ordinateur principal pour l’ordinateur spécifié.                                                                                                                                  |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                               | Disjoint un ordinateur d’un groupe de travail ou d’un domaine.                                                                                                                                            |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                               | Vérifie la validité d’un nom d’ordinateur, d’un nom de groupe de travail ou d’un nom de domaine.                                                                                                                   |



 

Pour plus d’informations sur la programmation pour Active Directory, consultez la [référence Active Directory](/windows/desktop/AD/active-directory-domain-services-reference). Pour plus d’informations sur les unités d’organisation, consultez [gestion des utilisateurs](/windows/desktop/AD/managing-users) dans la documentation Active Directory.

 

 