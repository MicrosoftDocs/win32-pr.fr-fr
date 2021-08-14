---
description: Une stratégie d’autorisation centrale collecte les règles d’autorisation spécifiques (CAPRs) dans une seule stratégie.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Stratégies d’autorisation centralisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0617f6bddb606d3c3fb3e5ccb6692c79c62a60f90de591b6ec3e04988db46f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783223"
---
# <a name="central-authorization-policies"></a>Stratégies d’autorisation centralisées

Une stratégie d’autorisation centrale collecte les règles d’autorisation spécifiques (CAPRs) dans une seule stratégie. Pour permettre la combinaison des règles d’autorisation spécifiques dans la stratégie d’autorisation holistique de l’organisation, CAPRs peut être référencé et appliqué à un ensemble de ressources. Pour ce faire, il faut collecter plusieurs (par référence) dans un capuchon. Une fois qu’une limite est définie, elle peut être distribuée consommée par les gestionnaires de ressources pour appliquer la stratégie d’autorisation des organisations aux ressources.

Un CAP a les attributs suivants :

-   Collection de CAPRs : liste de références aux objets CAPR existants
-   Identificateur (SID)
-   Description
-   Nom

Un capuchon est évalué lors de l’évaluation de l’accès pour les fichiers et dossiers sur lesquels un administrateur l’active. Lors d’un appel [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , la vérification de la limite est logiquement associée à la vérification de la liste de contrôle d’accès discrétionnaire. Cela signifie que pour obtenir l’accès à un fichier auquel l’extrémité s’applique, un utilisateur doit avoir accès à la fois en fonction de l’extrémité (son CAPRs associé) et à la liste de contrôle d’accès discrétionnaire sur le fichier.

Exemple d’extrémité :

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Définition de l’extrémité

Un capuchon est créé et modifié dans Active Directory à l’aide d’une nouvelle expérience utilisateur dans le Centre (ou PowerShell) qui permet à l’administrateur de créer un capuchon et de spécifier un ensemble de CAPRs qui composent l’extrémité.

 

 
