---
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsqu’un contact d’entrée est détecté.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualisation des contacts (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320253"
---
# <a name="contact-visualization"></a>Visualisation des contacts

Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsqu’un contact d’entrée est détecté.

Ces constantes sont utilisées avec les paramètres **SPI \_ GETCONTACTVISUALIZATION** et **SPI \_ SETCONTACTVISUALIZATION** et la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ désactivé**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Spécifie que les commentaires de l’interface utilisateur pour tous les contacts sont désactivés.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ sur**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour tous les contacts.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ mode**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour tous les contacts sur les visuels en mode présentation.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de configuration](configuration-constants.md)
</dt> <dt>

[**Visualisation de mouvement**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuration des commentaires en entrée](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

