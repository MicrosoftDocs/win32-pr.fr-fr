---
title: Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11
description: Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Plug-ins du lecteur Windows Media, Assistant plug-in
- plug-ins, Assistant de plug-in
- plug-ins de traitement de signal numérique, Assistant plug-in
- Plug-ins DSP, Assistant plug-in
- Assistant de plug-in
- Visual Studio, Assistant de plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381514"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11

Le kit de développement logiciel (SDK) du lecteur Windows Media 11 introduit les modifications suivantes dans l’Assistant de plug-in DSP :

-   Les plug-ins inscrivent le modèle de thread comme « les deux ». Cela permet au plug-in de s’exécuter dans le pipeline Media Foundation sous Windows Vista. Consultez le fichier *ProjectName*. RGS.

    -   Les plug-ins audio DSP prennent en charge les deux formats supplémentaires suivants :

    <!-- -->

    -   \_format Wave \_ IEEE \_ float
    -   \_Format Wave \_ extensible avec SUBformat KSDATAFORMAT sous- \_ type \_ IEEE \_ float.

    Consultez le fichier *ProjectName*. cpp.

    1.  Les plug-ins de vidéo DSP prennent en charge le format vidéo NV12.
    2.  Les plug-ins effectuent des appels supplémentaires à [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) et [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) avec un nouveau type de plug-in : WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC. Consultez le fichier *projectnamedll*. cpp du projet.
    3.  Un projet supplémentaire dans chaque solution crée une DLL proxy/stub pour l’interface personnalisée des paramètres de page de propriétés. Consultez le projet *projectnamePS* .
    4.  Les appels aux méthodes déconseillées ont été modifiés pour utiliser les versions les plus récentes.
    5.  L’Assistant peut générer un plug-in en mode double qui fonctionne à la fois en tant qu’DMO, en implémentant **IMediaObject** et en tant que MFT, en implémentant **IMFTransform**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Assistant de plug-in DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




