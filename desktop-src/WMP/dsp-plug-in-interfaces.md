---
title: Interfaces du plug-in DSP
description: Interfaces du plug-in DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Plug-ins du lecteur Windows Media, interfaces DSP
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces DSP
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- plug-ins de traitement de signal numérique, interface ISpecifyPropertyPage
- Plug-ins DSP, interfaces
- Plug-ins DSP, interface ISpecifyPropertyPage
- interfaces, plug-ins DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381675"
---
# <a name="dsp-plug-in-interfaces"></a>Interfaces du plug-in DSP

Les interfaces de plug-in Digital Signal Processing (DSP) sont utilisées pour gérer le transfert de données entre le lecteur Windows Media et le plug-in. Tous les plug-ins DSP peuvent éventuellement implémenter l’interface **ISpecifyPropertyPage** pour fournir une implémentation de page de propriétés.

Les interfaces suivantes sont requises pour la création de plug-ins DSP.



| Interface                                                | Description                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Gère l’échange de données avec le lecteur Windows Media et effectue des tâches de traitement de signal numérique. La documentation détaillée est incluse dans le kit de développement logiciel (SDK) DirectX. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Gère l’inscription du plug-in.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Gère la connexion au lecteur Windows Media.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Stocke si le plug-in est actuellement activé par le lecteur Windows Media.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Récupère des informations à partir du lecteur sur le temps de flux actuel et l’état du flux.                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de plug-ins DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




