---
description: Si ce bit est défini, la boîte de dialogue est modale, d’autres boîtes de dialogue de la même application ne peuvent pas être placées dessus et la boîte de dialogue garde le contrôle pendant son exécution.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de style de boîte de dialogue modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230250"
---
# <a name="modal-dialog-style-bit"></a>Bit de style de boîte de dialogue modal

Si ce bit est défini, la boîte de dialogue est modale, d’autres boîtes de dialogue de la même application ne peuvent pas être placées dessus et la boîte de dialogue garde le contrôle pendant son exécution. Si ce bit n’est pas défini, la boîte de dialogue est non modale, d’autres boîtes de dialogue de la même application peuvent être déplacées dessus. Après la création et l’affichage d’une boîte de dialogue non modale, l’interface utilisateur retourne le contrôle au programme d’installation. Le programme d’installation appelle ensuite l’interface utilisateur régulièrement pour mettre à jour la boîte de dialogue et lui permettre de traiter les messages. Dès que cette opération est effectuée, le contrôle est retourné au programme d’installation.

> [!Note]  
> Il ne doit y avoir aucune boîte de dialogue non modale dans une séquence d’Assistant, étant donné que cela retournerait le contrôle au programme d’installation, mettant fin à la séquence de l’Assistant prématurément.

 

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbDialogAttributesSysModal** |



 

 

 



