---
title: connexion à Lecteur Windows Media
description: connexion à Lecteur Windows Media
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- plug-ins Lecteur Windows Media, entrées de registre
- plug-ins, entrées de Registre
- plug-ins Lecteur Windows Media, connexion
- plug-ins, connexion
- plug-ins de traitement de signal numérique, connexion
- Plug-ins DSP, connexion
- plug-ins de traitement de signal numérique, entrées de Registre
- Plug-ins DSP, entrées de Registre
- Registre, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919399"
---
# <a name="connecting-to-windows-media-player"></a>connexion à Lecteur Windows Media

Lecteur Windows Media se connecte automatiquement aux plug-ins DSP qui ont été installés et correctement inscrits. les plug-ins DSP doivent appeler [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) pour créer les entrées de registre nécessaires pour permettre à Lecteur Windows Media de reconnaître le plug-in et de le répertorier sous l’onglet **plug-ins** de la boîte de dialogue Options. Pour supprimer les entrées de Registre créées par **IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin**, le plug-in appelle [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




