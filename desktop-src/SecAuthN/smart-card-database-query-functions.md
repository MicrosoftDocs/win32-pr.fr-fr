---
description: Interrogez la base de données de la carte à puce. Ils peuvent fournir une liste des cartes à puce fournies par un utilisateur spécifique, les interfaces et le fournisseur de services principal d’une carte spécifique, les groupes de lecteurs définis pour le système et les lecteurs au sein d’un ensemble de groupes de lecteurs.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Fonctions de requête de base de données de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324772"
---
# <a name="smart-card-database-query-functions"></a>Fonctions de requête de base de données de carte à puce

Les fonctions suivantes interrogent la [*base de données des cartes à puce*](../secgloss/s-gly.md). Ils peuvent fournir une liste des cartes à puce fournies par un utilisateur spécifique, les interfaces et le [*fournisseur de services principal*](../secgloss/p-gly.md) d’une carte spécifique, les [*groupes de lecteurs*](../secgloss/r-gly.md) définis pour le système et les [*lecteurs*](../secgloss/r-gly.md) au sein d’un ensemble de groupes de lecteurs.

Lorsque vous utilisez ces fonctions, vous pouvez interroger la base de données de carte à puce complète, ou vous pouvez affiner la recherche en définissant le [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md). Le contexte du gestionnaire de ressources est défini en appelant [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) avant d’appeler une fonction de requête.

> [!Note]  
> Sans un contexte spécifié, certaines informations peuvent toujours être inaccessibles en raison de restrictions de sécurité.

 



| Rubrique                                                  | Description                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Récupérez l’identificateur (GUID) du [*fournisseur de services principal*](../secgloss/p-gly.md) pour la carte donnée. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Récupérer une liste de cartes précédemment introduites dans le système par un utilisateur spécifique.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Récupérez les identificateurs (GUID) des interfaces fournies par une carte donnée.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Récupérez la liste des groupes de lecteurs qui ont été introduits précédemment dans le système.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Récupérez la liste des lecteurs dans un ensemble de groupes de lecteurs nommés.                                                                                                                    |



 

 

 
