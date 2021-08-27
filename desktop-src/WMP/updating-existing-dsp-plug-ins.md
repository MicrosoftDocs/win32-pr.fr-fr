---
title: Mise à jour des plug-ins DSP existants
description: Mise à jour des plug-ins DSP existants
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- plug-ins Lecteur Windows Media, traitement des signaux numériques (DSP)
- plug-ins, traitement des signaux numériques (DSP)
- plug-ins de traitement de signal numérique, mise à jour
- Plug-ins DSP, mise à jour
- versions de Lecteur Windows Media, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725a7a752206f4d321af9deb106df82c40b677dd719182660c5940cac4788244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122729"
---
# <a name="updating-existing-dsp-plug-ins"></a>Mise à jour des plug-ins DSP existants

les plug-ins DSP créés avant le lancement du kit de développement logiciel (SDK) Lecteur Windows Media 11 peuvent ne pas fonctionner comme prévu avec Lecteur Windows Media 11 s’exécutant sur Windows Vista. pour vous assurer que les clients qui exécutent Lecteur Windows Media 11 sur Windows Vista peuvent utiliser vos plug-ins, vous devez apporter certaines modifications à votre code de plug-in DSP, recompiler votre projet et distribuer le plug-in mis à jour à vos clients.

les projets créés à l’aide de la version la plus récente de l’assistant de plug-in Lecteur Windows Media contiendront les mises à jour requises. consultez [les mises à jour de l’assistant de Plug-in DSP pour Lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md). (il est judicieux d’exécuter l’assistant pour créer un exemple de projet, puis d’utiliser un outil comme Windiff.exe, fourni avec Visual Studio, pour inspecter les différences entre l’exemple de code et votre code de production.)

Trois modifications principales doivent être apportées à tous les plug-ins DSP existants :

-   Modifiez la façon dont le plug-in s’inscrit. Votre plug-in existant inscrit probablement le modèle de thread en tant que « cloisonnement ». Lecteur Windows Media 11 s’exécutant sur Windows Vista nécessite que les plug-ins DSP inscrivent le modèle de thread comme « Both ». Vous pouvez résoudre ce problème en modifiant la valeur du modèle de thread dans votre fichier *ProjectName*. RGS, comme suit :

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > La spécification du modèle de thread comme « both » supprime toute sérialisation fournie par COM pour les appels à des interfaces personnalisées. Si vous effectuez des appels à vos interfaces personnalisées à partir de plusieurs threads, vous devez fournir cette sérialisation vous-même.

     

    Lecteur Windows Media 11 garantit que les appels à DMO interfaces sont correctement sérialisés.

    1.  Ajoutez des appels à [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) et [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) avec un nouveau type de plug-in : WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC dans DllRegisterServer et DllUnregisterServer dans votre fichier *projectnamedll*. cpp. Pour plus d’informations, consultez les pages de référence pour ces méthodes.
    2.  Créez et distribuez une DLL proxy/stub pour activer le marshaling COM de toute interface personnalisée implémentée ou créée par la classe de plug-in. Une interface personnalisée est toute interface propriétaire que vous définissez et implémentez pour une utilisation par l’objet de plug-in. Cela inclut l’interface personnalisée utilisée par votre page de propriétés, si vous en avez fourni une, mais peut également inclure des interfaces qui se connectent aux plug-ins d’interface utilisateur, par exemple. *Iprojectname* est un exemple d’interface personnalisée créée par l’Assistant de plug-in. **IMediaObject** et **IWMPPluginEnable** sont des exemples d’interfaces qui ne sont pas des interfaces personnalisées.

Si votre plug-in DSP traite le son, vous devez également ajouter la prise en charge des nouveaux formats audio suivants :

-   \_format Wave \_ IEEE \_ float
-   \_Format Wave \_ extensible avec SUBformat KSDATAFORMAT sous- \_ type \_ IEEE \_ float.

Si votre plug-in DSP traite une vidéo, vous devez ajouter la prise en charge du format vidéo NV12.

Pour obtenir un exemple de traitement de ces types de format, consultez l’exemple de plug-in DSP audio ou Video créé par l’Assistant.

## <a name="about-the-proxystub-project"></a>À propos du Project de proxy/stub

La façon la plus simple de créer un projet DLL proxy/stub pour votre plug-in DSP consiste à exécuter l’Assistant de plug-in DSP. Cela permet de créer un exemple de projet de proxy/stub que vous pouvez modifier pour utiliser votre code existant. Vous devrez apporter les modifications suivantes :

1.  Supprimez les définitions existantes de vos interfaces personnalisées de votre code. par exemple, l’assistant de plug-in DSP du Lecteur Windows Media 10 SDK a créé la définition d’interface *Iprojectname* dans le fichier *projectname*. h à l’aide du mot clé **interface** .
2.  Définissez vos interfaces personnalisées dans le fichier IDL du projet proxy/stub.
3.  Générez le projet proxy/stub avant votre projet principal. vous pouvez configurer Visual Studio pour effectuer cette opération automatiquement si les deux projets font partie de la même solution.
4.  Le compilateur MIDL crée un nouveau fichier d’en-tête dont le nom est au format *ProjectName* \_ h.h. Vous devez inclure cet en-tête dans votre projet principal (dans *nom_projet*. h). Elle contient les définitions de vos interfaces personnalisées.

## <a name="distributing-the-updated-plug-in"></a>Distribution du plug-in mis à jour

Vous pouvez installer le plug-in mis à jour sur les ordinateurs de vos utilisateurs exactement comme vous l’avez déjà passé. Toutefois, vous devez maintenant également distribuer et inscrire la DLL proxy/stub.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




