---
title: ProgressBar
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de barre de progression.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b99a31bbbd3b80de0d528d5232c79c28af1e1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106529053"
---
# <a name="progress-bar"></a>ProgressBar

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles de barre de progression.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                            | Contenu                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Contrôle de barre de progression](progress-bar-control.md) | Une barre de progression est une fenêtre qu’une application peut utiliser pour indiquer la progression d’une longue opération.<br/> |



 

### <a name="messages"></a>Messages



| Rubrique                                       | Contenu                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DELTAPOS PBM**](pbm-deltapos.md)       | Avance la position actuelle d’une barre de progression d’un incrément spécifié et redessine la barre pour refléter la nouvelle position. <br/>                                                                                                                                 |
| [**\_GETBARCOLOR PBM**](pbm-getbarcolor.md) | Obtient la couleur de la barre de progression.<br/>                                                                                                                                                                                                                        |
| [**\_GETBKCOLOR PBM**](pbm-getbkcolor.md)   | Obtient la couleur d’arrière-plan de la barre de progression.<br/>                                                                                                                                                                                                             |
| [**\_GETPOS PBM**](pbm-getpos.md)           | Récupère la position actuelle de la barre de progression. <br/>                                                                                                                                                                                                       |
| [**\_GETRANGE PBM**](pbm-getrange.md)       | Récupère des informations sur les limites haute et basse actuelles d’un contrôle de barre de progression donné. <br/>                                                                                                                                                              |
| [**\_GETSTATE PBM**](pbm-getstate.md)       | Obtient l’état de la barre de progression.<br/>                                                                                                                                                                                                                        |
| [**\_GETSTEP PBM**](pbm-getstep.md)         | Récupère l’incrément d’étape d’une barre de progression. L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un message [**PBM \_ STEPIT**](pbm-stepit.md) .<br/>                                               |
| [**\_SETBARCOLOR PBM**](pbm-setbarcolor.md) | Définit la couleur de la barre de l’indicateur de progression dans le contrôle de barre de progression. <br/>                                                                                                                                                                                 |
| [**\_SETBKCOLOR PBM**](pbm-setbkcolor.md)   | Définit la couleur d’arrière-plan dans la barre de progression. <br/>                                                                                                                                                                                                            |
| [**\_SETMARQUEE PBM**](pbm-setmarquee.md)   | Définit la barre de progression en mode texte défilant. La barre de progression se déplace alors comme un texte défilant.<br/>                                                                                                                                                                |
| [**\_SetPos PBM**](pbm-setpos.md)           | Définit la position actuelle d’une barre de progression et redessine la barre pour refléter la nouvelle position. <br/>                                                                                                                                                             |
| [**PBM \_**](pbm-setrange.md)       | Définit les valeurs minimale et maximale d’une barre de progression et redessine la barre pour refléter la nouvelle plage.<br/>                                                                                                                                                       |
| [**\_SETRANGE32 PBM**](pbm-setrange32.md)   | Affecte une valeur 32 bits à la plage d’un contrôle de barre de progression. <br/>                                                                                                                                                                                               |
| [**PBM- \_ SETSTATE**](pbm-setstate.md)       | Définit l’état de la barre de progression.<br/>                                                                                                                                                                                                                        |
| [**\_SETSTEP PBM**](pbm-setstep.md)         | Spécifie l’incrément de l’étape d’une barre de progression. L’incrément d’étape correspond à la quantité d’augmentation de la position actuelle de la barre de progression à chaque fois qu’elle reçoit un message [**PBM \_ STEPIT**](pbm-stepit.md) . Par défaut, l’incrément de l’étape est défini sur 10. <br/> |
| [**\_STEPIT PBM**](pbm-stepit.md)           | Avance la position actuelle d’une barre de progression à l’aide de l’incrément de l’étape et redessine la barre pour refléter la nouvelle position. Une application définit l’incrément d’étape en envoyant le message [**PBM \_ SETSTEP**](pbm-setstep.md) . <br/>                                |



 

### <a name="structures"></a>Structures



| Rubrique                      | Contenu                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Contient des informations sur les limites haute et basse d’un contrôle de barre de progression. Cette structure est utilisée avec le message [**PBM \_ GETRANGE**](pbm-getrange.md) . <br/> |



 

### <a name="constants"></a>Constantes



| Rubrique                                                          | Contenu                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Styles de contrôle de barre de progression](progress-bar-control-styles.md) | Les styles de contrôle suivants sont pris en charge par les contrôles de **barre de progression** :<br/> |



 

 

 





