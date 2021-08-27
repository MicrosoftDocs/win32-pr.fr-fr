---
description: Le programme d’installation stocke toutes les informations relatives à l’interface utilisateur dans les tables de la base de données d’installation.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Aperçu de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738387ac834d4e9c26f4a413755dce0c5abdc5e421cc4ef88b1f9b41054f201d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082659"
---
# <a name="previewing-the-user-interface"></a>Aperçu de l’interface utilisateur

Le programme d’installation stocke toutes les informations relatives à l' [interface utilisateur](user-interface.md) dans les tables de la base de données d’installation. Pour faciliter la conception de l’interface utilisateur, le programme d’installation fournit également un mode d’aperçu pour afficher ces informations. La procédure suivante décrit comment activer le mode aperçu de l’interface utilisateur et afficher l’apparence actuelle des boîtes de dialogue et des panneaux.

**Pour afficher l’interface utilisateur en mode aperçu**

1.  Activez le mode aperçu en appelant la fonction [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .
2.  Affichez les boîtes de dialogue particulières en appelant la fonction [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .
3.  Affichez des panneaux d’affichage particuliers en appelant la fonction [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .

 

 



