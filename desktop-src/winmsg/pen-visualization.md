---
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements de stylet répertoriés est détecté.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualisation du stylet (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529163"
---
# <a name="pen-visualization"></a>Visualisation du stylet

Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements de stylet répertoriés est détecté.

Ces constantes sont utilisées avec les paramètres **SPI \_ GETPENVISUALIZATION** et **SPI \_ SETPENVISUALIZATION** et la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ désactivé**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements de stylet sont désactivés.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ sur**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements de stylet sont activés.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ Tap**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour un robinet Pen.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour un double-appui sur le stylet.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_curseur PENVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour le curseur de stylet.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de configuration](configuration-constants.md)
</dt> <dt>

[**Visualisation des contacts**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuration des commentaires en entrée](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

