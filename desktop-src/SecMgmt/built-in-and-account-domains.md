---
description: Décrit les domaines intégrés et de compte sur les systèmes Windows.
ms.assetid: 306c258b-950e-4506-99e2-67a3714285ff
title: Domaines intégrés et comptes de comptes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d2d4bb18e1ac2ea33aaff008475a44515d9231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523314"
---
# <a name="built-in-and-account-domains"></a>Domaines intégrés et comptes de comptes

Les domaines sur un système Windows appartiennent aux deux catégories suivantes :

-   [Ordinateurs qui ne sont pas des contrôleurs de domaine](#computers-that-are-not-domain-controllers)
-   [Ordinateurs qui sont des contrôleurs de domaine](#computers-that-are-domain-controllers)

## <a name="computers-that-are-not-domain-controllers"></a>Ordinateurs qui ne sont pas des contrôleurs de domaine

La base de données SAM (Security Accounts Manager) réside sur chaque ordinateur et gère les comptes pour le domaine intégré et le domaine du compte.



| Domain          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Domaine intégré | Ce domaine contient les groupes locaux par défaut, tels que les groupes administrateurs et utilisateurs, qui sont établis lors de l’installation du système d’exploitation. Le nom de ce domaine est une version localisée de BUILTIN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Domaine du compte  | Le domaine de compte peut contenir des comptes d’utilisateurs, de groupes et de groupes locaux. Le compte administrateur se trouve dans ce domaine. Les comptes définis dans le domaine de compte d’une station de travail ou d’un serveur membre sont limités à l’accès aux ressources situées sur l’ordinateur physique où se trouve le compte. Sur un système qui ne fait pas partie d’un réseau et qui, par conséquent, n’a pas de [domaine principal](primary-and-trusted-domains.md), le domaine du compte est utilisé pour héberger tous les comptes qui fournissent l’accès à l’ordinateur. Sur un système qui fait partie d’un réseau, le domaine du compte de l’ordinateur est utilisé pour héberger les comptes qui n’accèdent pas aux ressources réseau. Les comptes qui requièrent l’accès au réseau doivent être définis dans le domaine du compte d’un contrôleur de domaine.<br/> Le nom de ce domaine est affecté au moment de l’installation du système et est déterminé par le nom de l’ordinateur. Si le nom de l’ordinateur est modifié, le nom de domaine du compte n’est pas mis à jour tant que l’ordinateur n’est pas redémarré.<br/> |



 

## <a name="computers-that-are-domain-controllers"></a>Ordinateurs qui sont des contrôleurs de domaine

Les contrôleurs de domaine n’ont pas de domaines de compte ou intégrés. En outre, au lieu d’une base de données SAM, ces systèmes utilisent le service d’annuaire Microsoft Active Directory pour stocker les informations d’accès au compte. Pour plus d’informations, consultez [Active Directory](/windows/desktop/AD/active-directory-domain-services).

 

