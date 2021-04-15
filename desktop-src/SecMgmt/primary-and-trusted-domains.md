---
description: Les termes suivants décrivent les domaines qui existent sur les systèmes distants.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domaines principaux et approuvés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525719"
---
# <a name="primary-and-trusted-domains"></a>Domaines principaux et approuvés

Les termes suivants décrivent les domaines qui existent sur les systèmes distants.

-   [Domaine principal](#primary-domain)
-   [Domaine approuvé](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Domaine principal

Un domaine principal est le domaine qui est responsable de l’établissement de relations d’approbation supplémentaires et de l’exécution de l’authentification (ou pour la transmission d’une demande d’authentification à un domaine approuvé approprié). Les contrôleurs de domaine dans le domaine principal gèrent ou transmettent les demandes d’authentification qui proviennent de la station de travail.

Lorsque l’ouverture de session se produit, l’autorité LSA vérifie les informations d’authentification dans les domaines intégrés et de compte. Si le compte qui est connecté à ne figure pas dans l’un de ces domaines, la demande d’ouverture de session est transmise au domaine principal du système.

## <a name="trusted-domain"></a>Domaine approuvé

Un domaine approuvé est un domaine approuvé par le système local pour authentifier les utilisateurs. En d’autres termes, si un utilisateur ou une application est authentifié par un domaine approuvé, cette authentification est acceptée par tous les domaines qui approuvent le domaine d’authentification.

Chaque domaine subordonné a automatiquement une relation d’approbation bidirectionnelle avec le domaine principal. Par défaut, cette approbation est transitive, ce qui signifie que si un système approuve le domaine A, il approuve également tous les domaines approuvés par le domaine A. Les approbations à sens unique sont également prises en charge pour les systèmes d’exploitation antérieurs à Windows 2000, qui ne prennent pas en charge les approbations transitives bidirectionnelles.

L' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) a un type d’objet, [**trustedDomain**](the-trusteddomain-object-type.md), qui est utilisé pour stocker des informations sur les relations d’approbation, y compris le nom et l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du domaine approuvé, le compte dans le domaine à utiliser pour les demandes d’authentification, les demandes de traduction de nom et SID et les noms des contrôleurs de domaine dans le domaine approuvé.

Sur les contrôleurs de domaine, l’autorité LSA crée une instance d’un objet [**trustedDomain**](the-trusteddomain-object-type.md) pour chaque domaine approuvé par le système local.

Par exemple, si une station de travail Windows XP approuve un contrôleur de domaine Windows 2000 qui, à son tour, approuve quatre autres systèmes, la station de travail, connectée à l’aide d’une approbation transitive, aura cinq objets [**trustedDomain**](the-trusteddomain-object-type.md) sur son système local.

 

 
