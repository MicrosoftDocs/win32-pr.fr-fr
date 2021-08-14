---
description: Chaque objet Active Directory est associé à un descripteur de sécurité.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Droits d’accès aux services d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901c8eba5736750e0c91eb713993876c47858407110ca3c8ebc6ed8122e1b8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913762"
---
# <a name="directory-services-access-rights"></a>Droits d’accès aux services d’annuaire

Chaque objet Active Directory est associé à un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) . Un ensemble de droits d’un tiers de confiance spécifique aux objets de service d’annuaire peut être défini dans ces descripteurs de sécurité. Ces droits sont répertoriés dans le tableau suivant. Pour plus d’informations, consultez [contrôler les droits d’accès](/windows/desktop/AD/control-access-rights).



| Droits                                | Signification                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ Open<br/>            | Ouvrez un objet DS.<br/>                                                                                                                                                                                                                                                            |
| \_enfant ACTRL DS \_ Create \_<br/>   | Créez un objet DS enfant.<br/>                                                                                                                                                                                                                                                    |
| \_enfant ACTRL DS \_ Delete \_<br/>   | Supprimer un objet de service d’annuaire enfant.<br/>                                                                                                                                                                                                                                                    |
| \_liste ACTRL DS \_<br/>            | Énumérer un objet de service d’annuaire.<br/>                                                                                                                                                                                                                                                       |
| lecture de ACTRL \_ DS \_ \_<br/>      | Lire les propriétés d’un objet de service d’annuaire.<br/>                                                                                                                                                                                                                                          |
| PROP. d' \_ écriture ACTRL DS \_ \_<br/>     | Écrire les propriétés d’un objet DS.<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ Self<br/>            | Accès autorisé uniquement après validation des contrôles de droits pris en charge par l’objet. Cet indicateur peut être utilisé seul pour effectuer toutes les vérifications de droits validées de l’objet ou il peut être associé à un identificateur d’un droit validé spécifique pour effectuer uniquement cette vérification.<br/> |
| arborescence de suppression de ACTRL \_ DS \_ \_<br/>    | Supprimer une arborescence d’objets DS.<br/>                                                                                                                                                                                                                                                 |
| \_objet de \_ liste ACTRL DS \_<br/>    | Répertorie une arborescence d’objets DS.<br/>                                                                                                                                                                                                                                                   |
| \_ \_ accès au contrôle ACTRL DS \_<br/> | Accès autorisé uniquement après l’exécution des vérifications de droits étendus prises en charge par l’objet. Cet indicateur peut être utilisé seul pour effectuer toutes les vérifications de droits étendus sur l’objet ou il peut être combiné avec un identificateur d’un droit étendu spécifique pour effectuer uniquement cette vérification.<br/>    |



 

 

