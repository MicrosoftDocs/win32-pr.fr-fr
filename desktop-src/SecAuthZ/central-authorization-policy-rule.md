---
description: L’objectif de la règle de stratégie d’autorisation centrale (CAPR) est de fournir une définition à l’ensemble du domaine d’un aspect isolé de la stratégie d’autorisation des organisations.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Règle de stratégie d’autorisation centrale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5638633f655794464a9d603e1bb6a0380d2224170b9afe0f6314b1f8fee945b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783203"
---
# <a name="central-authorization-policy-rule"></a>Règle de stratégie d’autorisation centrale

L’objectif de la règle de stratégie d’autorisation centrale (CAPR) est de fournir une définition à l’ensemble du domaine d’un aspect isolé de la stratégie d’autorisation de l’organisation. L’administrateur définit le CAPR pour appliquer l’une des exigences d’autorisation spécifiques. Étant donné que le CAPR définit une seule exigence spécifique souhaitée de la stratégie d’autorisation, il peut être plus simplement défini et interprété que si toutes les exigences de la stratégie d’autorisation de l’organisation sont compilées dans une définition de stratégie unique.

CAPR a les attributs suivants :

-   Nom : identifie le CAPR pour les administrateurs.
-   Description : définit l’objectif du CAPR et toutes les informations qui peuvent être nécessaires aux consommateurs du CAPR.
-   Expression d’applicabilité : définit les ressources ou situations dans lesquelles la stratégie sera appliquée.
-   ID : identificateur à utiliser pour l’audit des modifications apportées au CAPR.
-   stratégie de Access Control Effective : descripteur de sécurité Windows contenant une liste DACL qui définit la stratégie d’autorisation effective.
-   Expression d’exception : une ou plusieurs expressions qui fournissent un moyen de remplacer la stratégie et d’accorder l’accès à un principal d’après l’évaluation de l’expression.
-   stratégie de préproduction : descripteur de sécurité facultatif Windows contenant une liste DACL qui définit une stratégie d’autorisation proposée (liste des entrées de contrôle d’accès) qui sera testée par rapport à la stratégie effective, mais non appliquée. S’il existe une différence entre les résultats de la stratégie effective et la stratégie de mise en lots, la différence est enregistrée dans le journal des événements d’audit.
    -   Étant donné que la mise en lots peut avoir un effet imprévisible sur les performances du système, un administrateur de stratégie de groupe doit être en mesure de sélectionner des ordinateurs spécifiques sur lesquels la mise en œuvre intermédiaire sera en vigueur. Cela permet à la stratégie existante d’être en place sur la plupart des ordinateurs d’une unité d’organisation pendant que la mise en lots se produit sur un sous-ensemble de machines.
    -   P2 : un administrateur local sur un ordinateur particulier doit être en mesure de désactiver la mise en lots si la mise en lots de cet ordinateur entraîne une dégradation des performances.
-   Lien secondaire à CAP : liste des liens vers les liens vers toutes les majuscules qui peuvent faire référence à ce CAPR.

Au cours de la vérification de l’accès, l’applicabilité du CAPR est évaluée en fonction de l’expression d’applicabilité. Si un CAPR est applicable, il est évalué pour déterminer s’il fournit à l’utilisateur demandeur l’accès demandé à la ressource identifiée. Les résultats de l’évaluation du Cap sont ensuite joints logiquement par **et** avec les résultats de la liste DACL sur la ressource et les autres CAPRs applicables en vigueur sur la ressource.

Exemple de CAPRs :

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a>Refuser les ACE dans CAPEs

dans Windows 8 les entrées ace de refus ne sont pas prises en charge dans un CAPR. L’expérience utilisateur de création de CAPR n’autorise pas la création d’une entrée du contrôle d’accès. En outre, lorsque l’autorité LSA récupère le CAP à partir de Active Directory, LSA vérifie qu’aucun CAPRs n’a de refus d’entrées de contrôle d’autorisation. Si une entrée du contrôle d’accès est détectée dans un CAPR, la limite est traitée comme étant non valide et ne sera pas copiée dans le registre ou le SRM.

> [!Note]  
> La vérification de l’accès n’impose pas l’absence d’ACE de refus. Les ACE de refus dans un CAPR seront appliqués. Il est prévu que les outils de création empêchent cela de se produire.

 

## <a name="cape-definition"></a>Définition du Cap

Les CAPRs sont créés par le biais d’une nouvelle expérience utilisateur fournie dans Centre d’administration Active Directory (le centre.) Dans le centre, une nouvelle option de tâche est fournie pour créer un CAPR. Lorsque cette tâche est sélectionnée, le centre invite l’utilisateur à fournir un nom de CAPR et une description à l’utilisateur. Lorsqu’ils sont fournis, les contrôles permettant de définir les autres éléments CAPR sont activés. Pour chacun des éléments restants de CAPR, l’expérience utilisateur appellera la liste de contrôle d’accès (ACL) pour permettre la définition de l’expression et/ou des ACL.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Scénario de Access Control dynamique (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
