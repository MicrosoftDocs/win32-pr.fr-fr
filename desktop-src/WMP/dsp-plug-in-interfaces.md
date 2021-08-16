---
title: Interfaces du plug-in DSP
description: Interfaces du plug-in DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- plug-ins Lecteur Windows Media, interfaces DSP
- plug-ins Lecteur Windows Media, interfaces
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
ms.openlocfilehash: c3bd030b09377adfe965698d6c411f1a39a745979f2db2eae9f0c613cad843d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863369"
---
# <a name="dsp-plug-in-interfaces"></a>Interfaces du plug-in DSP

les interfaces de plug-in de traitement de signal numérique (DSP) sont utilisées pour gérer le transfert de données entre Lecteur Windows Media et le plug-in. Tous les plug-ins DSP peuvent éventuellement implémenter l’interface **ISpecifyPropertyPage** pour fournir une implémentation de page de propriétés.

Les interfaces suivantes sont requises pour la création de plug-ins DSP.



| Interface                                                | Description                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | gère l’échange de données avec Lecteur Windows Media et effectue des tâches de traitement de signal numérique. La documentation détaillée est incluse dans le kit de développement logiciel (SDK) DirectX. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Gère l’inscription du plug-in.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | gère la connexion à Lecteur Windows Media.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | stocke si le plug-in est actuellement activé par Lecteur Windows Media.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Récupère des informations à partir du lecteur sur le temps de flux actuel et l’état du flux.                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de plug-ins DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




