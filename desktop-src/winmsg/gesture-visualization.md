---
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements répertoriés est détecté.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualisation des mouvements (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538935"
---
# <a name="gesture-visualization"></a>Visualisation de mouvement

Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements répertoriés est détecté.

Ces constantes sont utilisées avec les paramètres **SPI \_ GETGESTUREVISUALIZATION** et **SPI \_ SETGESTUREVISUALIZATION** et la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**Remarque**  

Pour récupérer ou définir des informations de visualisation du stylet, nous vous recommandons d’utiliser les paramètres **SPI \_ GETPENVISUALIZATION** et **SPI \_ SETPENVISUALIZATION** , ainsi que les constantes répertoriées dans la [**visualisation du stylet**](pen-visualization.md).

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ désactivé**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements sont désactivés.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ sur**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements sont activés.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION \_ Tap**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour un TAP.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour un double-clic.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour une pression et un TAP.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour une pression et un blocage.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Spécifie les commentaires de l’interface utilisateur pour un TAP droit.


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

[**Visualisation des contacts**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuration des commentaires en entrée](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

