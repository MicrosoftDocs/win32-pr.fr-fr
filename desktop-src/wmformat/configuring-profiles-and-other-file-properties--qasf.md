---
title: Configuration des profils et des autres propriétés de fichier (QASF)
description: Configuration des profils et des autres propriétés de fichier (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, configuration de profils (QASF)
- Windows Media Format SDK, configuration des propriétés de fichier (QASF)
- Windows Media Format SDK, Metadata (QASF)
- ASF (Advanced Systems Format), configuration des profils (QASF)
- ASF (format des systèmes avancés), configuration des profils (QASF)
- ASF (Advanced Systems Format), configuration des propriétés de fichier (QASF)
- ASF (format des systèmes avancés), configuration des propriétés de fichier (QASF)
- ASF (Advanced Systems Format), métadonnées (QASF)
- ASF (format des systèmes avancés), métadonnées (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- métadonnées, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219625"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a>Configuration des profils et des autres propriétés de fichier (QASF)

Les éléments suivants décrivent comment effectuer diverses tâches liées à la création de fichiers ASF.

## <a name="creating-a-profile-qasf"></a>Création d’un profil (QASF)

pour créer un profil personnalisé, utilisez directement le kit de développement logiciel (SDK) de Format multimédia Windows pour créer un objet de gestionnaire de profils à l’aide de la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Ensuite, créez le profil et transmettez-le à l' [enregistreur WM ASF](wm-asf-writer-filter.md) à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . il s’agit de la seule façon de configurer le filtre avec un profil qui utilise les codecs de série Windows Media Audio et Video 9. Les profils système des versions antérieures de ces codecs peuvent être ajoutés à l’aide de la méthode [**IConfigASFWriter :: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .

## <a name="adding-metadata-qasf"></a>Ajout de métadonnées (QASF)

Pour ajouter des métadonnées à un fichier, appelez **QueryInterface** à partir de l’interface **IBaseFilter** sur le [writer WM ASF](wm-asf-writer-filter.md) pour récupérer l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) . Une fois que le filtre a reçu un profil, utilisez les méthodes de l’interface **IWMHeaderInfo** pour écrire les métadonnées.

## <a name="indexing-a-file-qasf"></a>Indexation d’un fichier (QASF)

L’enregistreur ASF WM crée par défaut des fichiers indexés de façon temporelle. Pour créer un fichier d’index de frames, utilisez la méthode [**IConfigAsfWriter :: SetIndexMode**](iconfigasfwriter-setindexmode.md) pour désactiver l’indexation, puis créez le fichier. une fois Windows l’opération terminée, utilisez le kit de développement logiciel (SDK) de Format multimédia directement pour créer un index basé sur des frames pour le fichier.

## <a name="performing-two-pass-encoding-qasf"></a>Exécution de l’encodage Two-Pass (QASF)

l’encodage en deux passes est pris en charge uniquement sur Windows codecs multimédias de la version 8 et versions ultérieures. Placez le writer WM ASF en mode prétraitement en appelant [**IConfigAsfWriter2 :: setParam**](iconfigasfwriter2-setparam.md) et en spécifiant am \_ CONFIGASFWRITER \_ param \_ Multipass dans le paramètre *DwParam* et **true** dans le paramètre *dwParam1* .

Exécutez ensuite le graphique de filtre. Lorsque toutes les étapes de prétraitement sont effectuées (en général, une seule passe de prétraitement est effectuée), l’application reçoit un événement de **\_ \_ fin de prétraitement EC** du filtre. Lorsque cet événement est reçu, utilisez **IMediaSeeking :: SetPositions** pour réinitialiser le pointeur de flux jusqu’au début, puis exécutez à nouveau le graphique de filtre. Après la dernière passe (en général, la deuxième passe), l’application reçoit un événement **EC \_ Complete** pour signifier que le processus d’encodage est terminé. Si une passe de prétraitement est annulée avant la réception de l’événement de **\_ prétraitement \_** de l’UE, appelez [**IConfigAsfWriter2 :: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) pour réinitialiser le filtre avant de tenter une autre exécution de prétraitement.

Il est uniquement nécessaire d’appeler **IConfigAsfWriter :: setParam**(am \_ CONFIGASFWRITER \_ param \_ Multipass, **false**) si vous souhaitez que le filtre soit complètement en mode de prétraitement.

> [!IMPORTANT]
> Il incombe à l’application d’activer le mode de prétraitement en fonction du profil qui sera utilisé pour l’encodage. Certains profils nécessitent un encodage en deux passes ; Si vous tentez d’encoder un fichier à l’aide d’un profil de ce type et que vous ne définissez pas AM \_ CONFIGASFWRITER \_ param \_ Multipass sur **true**, une \_ erreur EC USERABORT est générée. Pour plus d’informations sur la façon de déterminer si un profil donné requiert un encodage en deux passes, consultez [utilisation de l’encodage Two-Pass](using-two-pass-encoding.md) ou écriture d’une [vitesse de transmission variable flux](writing-variable-bit-rate-streams.md).

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>Obtention et définition des propriétés de la mémoire tampon au moment de l’exécution (QASF)

dans certains scénarios, par exemple, si vous souhaitez forcer l’insertion d’une image clé lors de l’écriture d’un fichier, une application peut avoir besoin d’obtenir ou de définir des informations sur une mémoire tampon de média Windows au moment de l’exécution. Le [lecteur ASF WM](wm-asf-reader-filter.md) et les filtres d' [enregistreur ASF WM](wm-asf-writer-filter.md) prennent tous deux en charge un mécanisme de rappel qui permet à une application d’accéder à l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) sur chaque mémoire tampon de média individuelle lors de la lecture ou de l’écriture de fichiers. Les applications peuvent utiliser cette interface pour désigner des exemples spécifiques en tant qu’images clés, ou [*cleanpoints*](wmformat-glossary.md), pour définir des codes temporels SMPTE, pour spécifier des paramètres d’entrelacement ou pour ajouter n’importe quel type de données privées à un flux.

Utilisez l’interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) pour vous inscrire aux rappels à partir du code confidentiel qui gère le flux vidéo. Lorsque le code PIN appelle votre méthode [**IAMWMBufferPassCallback :: Notify**](iamwmbufferpasscallback-notify.md) , examinez les horodatages sur la mémoire tampon et, le cas échéant, appelez [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) pour définir la propriété de **\_ \_ OutputCleanPoint WM SampleExtensionGUID** sur la mémoire tampon sur **true**.

## <a name="non-square-pixel-support-qasf"></a>Prise en charge des pixels non carrés (QASF)

L’enregistreur ASF WM se connecte à un filtre en amont, tel que le décodeur DV, qui génère des informations sur les proportions en pixels. L’enregistreur ASF WM écrira ces informations en tant qu’extensions d’unité de données pour chaque exemple dans le fichier.

Lorsque le lecteur ASF WM rencontre des informations sur les proportions de pixels dans l’en-tête de fichier ou dans les extensions d’unité de données pour les exemples, il propose un type de média **VIDEOINFOHEADER2** comme premier choix sur sa broche de sortie. Les membres **dwPictAspectRatioX** et **dwPictAspectRatioY** de la structure, qui décrivent les proportions du rectangle vidéo, sont correctement ajustés pour prendre en compte les proportions en pixels.

## <a name="maintaining-interlaced-format"></a>Conserver le format entrelacé

Si vous capturez une vidéo entrelacée à partir d’une télévision ou d’une caméra DV, vous souhaiterez peut-être conserver la vidéo d’origine en tant que champs indépendants Si vous vous attendez à ce que le fichier encodé soit lu sur une télévision ou un autre périphérique d’affichage entrelacé. (Les moniteurs d’ordinateur sont des périphériques d’analyse progressive.) Si vous désentrelacez une vidéo, puis la réentrelacer pour la lire sur une télévision, une perte de données est générée. Dans un fichier ASF, les informations d’entrelacement sont stockées en tant qu’extensions d’unité de données que l’application applique à chaque exemple à l’aide de la méthode **IAMWMBufferPassCallback** décrite précédemment. Pour encoder un fichier qui conserve les paramètres d’entrelacement d’origine, procédez comme suit :

-   Implémentez une classe qui prend en charge **IAMWMBufferPassCallback** et écrivez une fonction Notify qui définit les indicateurs entrelacés pour chaque exemple. Cette fonction sera appelée par l’enregistreur ASF WM avant de traiter chaque exemple.


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   Définissez les extensions d’unité de données sur le profil avant de passer le profil au filtre.


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   Après avoir configuré le filtre avec le profil, obtenez l’interface **IWMWriterAdvanced2** à partir de l’enregistreur ASF WM et appelez la méthode **SetInputSettings** .

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 