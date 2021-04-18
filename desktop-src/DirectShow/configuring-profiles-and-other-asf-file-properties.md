---
description: Configuration de profils et autres propriétés de fichier ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configuration de profils et autres propriétés de fichier ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392728"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>Configuration de profils et autres propriétés de fichier ASF

Les éléments suivants décrivent comment effectuer diverses tâches liées à la création de fichiers ASF. Certaines des interfaces mentionnées dans cette rubrique sont documentées dans la documentation du kit de développement logiciel (SDK) Windows Media format.

Création d’un profil

Les profils ASF sont présentés en détail dans le kit de développement logiciel (SDK) de format Windows Media. Fondamentalement, ils décrivent les attributs d’un fichier au format Windows Media, tels que la vitesse de transmission, le nombre et le type de flux, ainsi que la qualité de compression. Le filtre utilise le profil pour déterminer le type de fichier de format Windows Media à écrire, le nombre de broches d’entrée qu’il doit configurer et les types de médias qu’il peut accepter.

Pour créer un profil personnalisé, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer un objet de gestionnaire de profils à l’aide de la fonction **WMCreateProfileManager** . Ensuite, créez le profil et transmettez-le à l' [enregistreur WM ASF](wm-asf-writer-filter.md) à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) . Il s’agit de la seule façon de configurer le filtre avec un profil qui utilise les codecs de série Windows Media Audio et Video 9. Les profils système des versions antérieures de ces codecs peuvent être ajoutés à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .

Vous pouvez réinitialiser le profil alors que les broches d’entrée du filtre sont connectées, à condition que le nouveau profil ne nécessite pas de broches d’entrée supplémentaires. Par exemple, si vous modifiez le profil d’un profil audio à entrée unique en un profil audio et vidéo à deux entrées, seul le code confidentiel audio sera reconnecté et aucun nouveau code confidentiel ne sera créé pour le flux vidéo.

Ajout de métadonnées

Pour ajouter des métadonnées à un fichier, interrogez le filtre du [writer WM ASF](wm-asf-writer-filter.md) pour l’interface **IWMHeaderInfo** . Une fois que le filtre a reçu un profil, utilisez les méthodes de l’interface **IWMHeaderInfo** pour écrire les métadonnées.

Indexation d’un fichier

L’enregistreur ASF WM crée par défaut des fichiers indexés de façon temporelle. Pour créer un fichier d’index de frames, utilisez la méthode [**IConfigAsfWriter :: SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) pour désactiver l’indexation, puis créez le fichier. Une fois l’opération terminée, utilisez le kit de développement logiciel (SDK) de format Windows Media directement pour créer un index basé sur des frames pour le fichier.

Encodage Two-Pass

L’encodage en deux passes est pris en charge uniquement sur les codecs Windows Media version 8 et versions ultérieures. Placez le writer WM ASF en mode prétraitement en appelant [**IConfigAsfWriter2 :: setParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) et en spécifiant am \_ CONFIGASFWRITER \_ param \_ Multipass dans le paramètre *DwParam* et **true** dans le paramètre *dwParam1* .

Exécutez ensuite le graphique de filtre. Lorsque toutes les étapes de prétraitement sont effectuées (en général, une seule passe de prétraitement est effectuée), l’application reçoit un événement de [**\_ \_ fin de prétraitement EC**](ec-preprocess-complete.md) du filtre. Lorsque cet événement est reçu, utilisez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) pour réinitialiser le pointeur de flux jusqu’au début, puis exécutez à nouveau le graphique de filtre. Après la dernière passe (en général, la deuxième passe), l’application reçoit un événement [**EC \_ Complete**](ec-complete.md) pour signifier que le processus d’encodage est terminé. Si une passe de prétraitement est annulée avant la réception de l’événement de **\_ prétraitement \_** de l’UE, appelez [**IConfigAsfWriter2 :: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) pour réinitialiser le filtre avant de tenter une autre exécution de prétraitement.

Il est nécessaire uniquement de définir le \_ paramètre am CONFIGASFWRITER \_ param \_ Multipass sur **false** si vous souhaitez que le filtre soit complètement en mode de prétraitement.

> [!IMPORTANT]
> Il incombe à l’application d’activer le mode de prétraitement en fonction du profil qui sera utilisé pour l’encodage. Certains profils nécessitent un encodage en deux passes ; Si vous tentez d’encoder un fichier à l’aide d’un profil de ce type et que vous ne définissez pas AM \_ CONFIGASFWRITER \_ param \_ Multipass sur **true**, une erreur [**EC \_ USERABORT**](ec-userabort.md) est générée. Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Windows Media format.

 

Obtention et définition des propriétés de la mémoire tampon au moment de l’exécution

Dans certains scénarios, par exemple, si vous souhaitez forcer l’insertion d’une image clé lors de l’écriture d’un fichier, une application peut avoir besoin d’obtenir ou de définir des informations sur un tampon Windows Media au moment de l’exécution. Le [lecteur ASF WM](wm-asf-reader-filter.md) et les filtres d' [enregistreur ASF WM](wm-asf-writer-filter.md) prennent tous deux en charge un mécanisme de rappel qui permet à une application d’accéder à l’interface **INSSBuffer3** sur chaque mémoire tampon de média individuelle lors de la lecture ou de l’écriture de fichiers. Les applications peuvent utiliser cette interface pour désigner des exemples spécifiques en tant qu’images clés, définir des codes temporels SMPTE, spécifier des paramètres d’entrelacement ou ajouter n’importe quel type de données privées à un flux.

Utilisez l’interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) pour vous inscrire aux rappels à partir du code confidentiel qui gère le flux vidéo. Le code PIN appellera votre méthode [**IAMWMBufferPassCallback :: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) pour chaque mémoire tampon.

Pixels non carrés

L’enregistreur ASF WM se connecte à un filtre en amont, tel que le décodeur DV, qui génère des informations sur les proportions en pixels. L’enregistreur ASF WM écrira ces informations en tant qu’extensions d’unité de données pour chaque exemple dans le fichier.

Lorsque le lecteur ASF WM rencontre des informations sur les proportions de pixels dans l’en-tête de fichier ou dans les extensions d’unité de données pour les exemples, il propose un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) comme premier choix sur sa broche de sortie. Les membres **dwPictAspectRatioX** et **dwPictAspectRatioY** de la structure, qui décrivent les proportions du rectangle vidéo, sont correctement ajustés pour prendre en compte les proportions en pixels.

Conserver le format entrelacé

Si vous capturez une vidéo entrelacée à partir d’une télévision ou d’une caméra DV, vous souhaiterez peut-être conserver la vidéo d’origine en tant que champs indépendants Si vous vous attendez à ce que le fichier encodé soit lu sur une télévision ou un autre périphérique d’affichage entrelacé. (Les moniteurs d’ordinateur sont des périphériques d’analyse progressive.) Si vous désentrelacez une vidéo, puis la réentrelacer pour la lire sur une télévision, une perte de données est générée. Dans un fichier ASF, les informations d’entrelacement sont stockées en tant qu’extensions d’unité de données que l’application applique à chaque exemple à l’aide de la méthode [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) décrite précédemment. Pour encoder un fichier qui conserve les paramètres d’entrelacement d’origine, procédez comme suit :

1.  Implémentez une classe qui prend en charge **IAMWMBufferPassCallback** et écrivez une fonction Notify qui définit les indicateurs entrelacés pour chaque exemple. Cette fonction sera appelée par l’enregistreur ASF WM avant de traiter chaque exemple.
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  Définissez les extensions d’unité de données sur le profil avant de passer le profil au filtre.
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  Après avoir configuré le filtre avec le profil, obtenez l’interface **IWMWriterAdvanced2** à partir de l’enregistreur ASF WM et appelez la méthode **SetInputSettings** .

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



