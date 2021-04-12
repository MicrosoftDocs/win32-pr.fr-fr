---
description: Gérez la base de données de la carte à puce, en mettant à jour la base de données à l’aide d’un contexte Resource Manager spécifié.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Fonctions de gestion de base de données de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319898"
---
# <a name="smart-card-database-management-functions"></a>Fonctions de gestion de base de données de carte à puce

Les fonctions suivantes gèrent la [*base de données des cartes à puce*](../secgloss/s-gly.md), en mettant à jour la base de données à l’aide d’un [*contexte Resource Manager*](../secgloss/r-gly.md)spécifié.

> [!Note]  
> La sécurité de la base de données est conservée en plaçant des restrictions d’accès sur la base de données, plutôt que d’ajouter des mécanismes de sécurité au [*sous-système de carte à puce*](../secgloss/s-gly.md).

 



| Rubrique                                                            | Description                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardAddReaderToGroup**](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | Ajoutez un [*lecteur*](../secgloss/r-gly.md) à un [*groupe de lecteurs*](../secgloss/r-gly.md). |
| [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | Retirez une carte à puce du système.                                                                                                                                    |
| [**SCardForgetReader**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | Suppression d’un lecteur du système.                                                                                                                                        |
| [**SCardForgetReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | Suppression d’un groupe de lecteurs du système.                                                                                                                                  |
| [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | Introduisez une nouvelle carte pour le système.                                                                                                                                     |
| [**SCardIntroduceReader**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | Introduisez un nouveau lecteur sur le système.                                                                                                                                   |
| [**SCardIntroduceReaderGroup**](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | Introduisez un nouveau groupe de lecteurs sur le système.                                                                                                                             |
| [**SCardRemoveReaderFromGroup**](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | Suppression d’un lecteur d’un groupe de lecteurs.                                                                                                                                    |



 

 

 
