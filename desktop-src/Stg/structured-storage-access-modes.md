---
title: Modes d’accès de stockage structuré
description: Les mécanismes de contrôle de l’accès simultané à un objet, par plusieurs processus et utilisateurs, sont essentiels.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Stockage structuré Strctd STG, notions de base, fonctions API, indicateurs pour l’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106521801"
---
# <a name="structured-storage-access-modes"></a>Modes d’accès de stockage structuré

Les mécanismes de contrôle de l’accès simultané à un objet, par plusieurs processus et utilisateurs, sont essentiels. COM fournit ces mécanismes en définissant les modes d’accès pour les objets de stockage et de flux. Le mode d’accès spécifié pour un objet de stockage parent est hérité par ses enfants, bien que vous puissiez placer des restrictions supplémentaires sur le flux ou le stockage enfant. Un objet de flux ou de stockage imbriqué peut être ouvert dans le même mode ou dans un mode plus restreint que celui de son parent, mais il ne peut pas être ouvert en mode moins restreint que celui de son parent.

Vous spécifiez les modes d’accès à l’aide des valeurs indiquées dans [**constantes STGM**](stgm-constants.md). Ces valeurs servent d’indicateurs à passer comme arguments aux méthodes de l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et aux fonctions API associées. En règle générale, plusieurs indicateurs sont combinés dans le paramètre *grfMode*, à l’aide d’une opération **or** booléenne.

Les indicateurs sont répartis en six groupes. Un seul indicateur de chaque groupe peut être spécifié à la fois :

-   [Indicateurs de transaction](transaction-flags.md)
-   [Indicateurs de création de stockage](storage-creation-flags.md)
-   [Indicateurs de création temporaires](temporary-creation-flags.md)
-   [Indicateurs de priorité](priority-flags.md)
-   [Indicateurs d’autorisation d’accès](access-permission-flags.md)
-   [Indicateurs d’accès partagé](shared-access-flags.md)

 

 




