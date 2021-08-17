---
description: L’interface IX509EndorsementKey expose les propriétés suivantes.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propriétés IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d135205680e4c998c1157844cfa66a9ef9bd7ef4df5ff8258a31e562a685e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117776187"
---
# <a name="ix509endorsementkey-properties"></a>Propriétés IX509EndorsementKey

L’interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expose les propriétés suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                        | Description                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Length, propriété**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Longueur en bits de la clé de type EK. Vous ne pouvez accéder à cette propriété qu’après l’appel de la méthode [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                                                                                                                            |
| [**Propriété ouverte**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indique si la méthode d' [**ouverture**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) a été appelée avec succès.<br/>                                                                                                                                                                                                                                            |
| [**ProviderName, propriété**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Nom du fournisseur de chiffrement. La valeur par défaut est le fournisseur de chiffrement de la plateforme Microsoft. Vous devez définir la propriété [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) avant d’appeler la méthode [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) . Vous ne pouvez pas modifier la propriété **providerName** après avoir appelé la méthode **Open** .<br/> |



 

 

 




