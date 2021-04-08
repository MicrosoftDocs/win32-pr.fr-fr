---
description: Objet qui encapsule plusieurs DSP associés à la capture vocale.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP de capture vocale (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755228"
---
# <a name="voice-capture-dsp"></a>DSP de capture vocale

Objet qui encapsule plusieurs DSP associés à la capture vocale.

## <a name="clsid"></a>CLSID

CLSID \_ CWMAudioAEC

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **IPropertyStore**

## <a name="properties"></a>Propriétés



| Propriété                                                                                     | Description                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [\_index d' \_ appareils MFPKEY WMAAECMA \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Spécifie les périphériques audio utilisés par DMO pour la capture et le rendu audio.                     |
| [\_GUID MFPKEY WMAAECMA \_ DEVICEPAIR \_](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifie la combinaison de périphériques audio actuellement utilisée par l’application.              |
| [\_ \_ \_ mode Source MFPKEY WMAAECMA \_ DMO](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Spécifie si DMO utilise le mode source ou le mode filtre.                                        |
| [MFPKEY \_ WMAAECMA \_ fonceur \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Spécifie le nombre de fois où DMO effectue la suppression de l’écho acoustique (AES) sur le signal résiduel. |
| [MFPKEY \_ WMAAECMA \_ Fonct, \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Spécifie si DMO effectue un contrôle d’augmentation automatique.                                        |
| [\_clip du \_ \_ Centre \_ d’MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Spécifie si DMO effectue un découpage central.                                               |
| [longueur de l' \_ \_ écho du Feature WMAAECMA MFPKEY \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Spécifie la durée d’écho que l’algorithme d’annulation de l’écho acoustique (AEC) peut gérer.    |
| [\_taille du \_ \_ frame \_ de MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Spécifie la taille du cadre audio.                                                                   |
| [MFPKEY \_ WMAAECMA \_ fonceur \_ MICARR \_](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Spécifie la poutre utilisée par DMO pour le traitement du tableau de microphone.                                |
| [\_ \_ \_ mode MICARR MFPKEY WMAAECMA \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Spécifie la manière dont DMO effectue le traitement du tableau de microphone.                                       |
| [MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ préproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Spécifie si DMO effectue le prétraitement des tableaux de microphones.                                |
| [\_remplissage du \_ \_ bruit \_ du MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Spécifie si DMO effectue un remplissage de bruit.                                                 |
| [MFPKEY \_ WMAAECMA \_ Feature \_](mfpkey-wmaaecma-featr-nsproperty.md)                          | Spécifie si DMO effectue la suppression du bruit.                                             |
| [\_VAD MFPKEY WMAAECMA \_ Fonct \_](mfpkey-wmaaecma-featr-vadproperty.md)                        | Spécifie le type de détection d’activité vocale effectuée par DMO.                             |
| [MODE de fonctionnalité de MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Permet à l’application de remplacer les paramètres par défaut de différentes propriétés.                   |
| [\_ \_ \_ limiteur de gain MFPKEY WMAAECMA MIC \_](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Spécifie si la méthode DMO applique la limite d’augmentation du microphone.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Spécifie la géométrie du tableau du microphone.                                                          |
| [\_ \_ métriques de qualité MFPKEY WMAAECMA \_](mfpkey-wmaaecma-quality-metricsproperty.md)            | Récupère les mesures de qualité pour AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ récupérer \_ les \_ statistiques TS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Spécifie si DMO stocke des statistiques de datage dans le registre.                           |
| [\_ \_ mode système MFPKEY \_ WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md)                    | Définit le mode de traitement.                                                                         |



 

## <a name="remarks"></a>Notes

Contrairement aux autres DSP, l’objet de capture vocale encapsule plusieurs DSP dans un objet unique, et l’objet est un objet DMO uniquement (il n’implémente pas [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). La capture vocale DMO comprend les composants DSP suivants :

-   Annulation de l’écho acoustique (AEC)
-   Traitement du tableau du microphone
-   Suppression du bruit
-   Contrôle du gain automatique
-   Détection de l’activité vocale

Les applications peuvent activer et désactiver chaque composant individuellement.

La capture vocale DMO prend en charge deux modes d’opération : le mode *filtre* et le mode *source* . En mode filtre, l’application envoie des échantillons audio à partir du microphone et de la ligne de haut-parleur à la requête DMO, et la requête DMO produit une sortie.

En mode Source, l’application n’a pas besoin de fournir des exemples à DMO. Au lieu de cela, DMO gère toutes les opérations sur les périphériques audio, y compris l’initialisation des appareils, la capture et la synchronisation des flux audio, le calcul des horodatages et la récupération de la géométrie du tableau du microphone. En utilisant le mode Source, l’application configure simplement DMO, et la sortie de l’DMO est un signal de microphone propre et traité. Le mode source est beaucoup plus facile à utiliser que le mode filtre, et est recommandé pour la plupart des applications.

Actuellement, la capture de voix DMO ne prend en charge que l’annulation de l’écho acoustique (AEC) à canal unique. la sortie de la ligne de haut-parleur doit être monocanal. Si le traitement du tableau de microphone est désactivé, l’entrée multicanal est repliée sur un canal pour le traitement AEC. Si le traitement du tableau de microphone et le traitement AEC sont activés, l’AEC est exécuté sur chaque élément de microphone avant le traitement du tableau de microphone.

### <a name="microphone-array-processing"></a>Traitement du tableau du microphone

Un tableau de microphone est un ensemble de microphones étroitement positionnés. Les tableaux de microphones offrent une meilleure direction qu’un seul microphone, car les ondes acoustiques arrivent à chaque microphone à une heure légèrement différente. Pour plus d’informations sur les tableaux de microphones, consultez les articles Web [prise en charge des tableaux de microphone dans Windows Vista](/windows-hardware/design/component-guidelines/audio) et [comment créer et utiliser des tableaux de microphone pour Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Utilisation du DSP de capture vocale

Pour utiliser le DSP de capture vocale, procédez comme suit.

### <a name="1-initialize-the-dmo"></a>1. initialiser le DMO

Créez la capture vocale DMO en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec le CLSID **CLSID \_ CWMAudioAEC**. Le DSDP de capture vocale expose uniquement les interfaces [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) et [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , de sorte qu’il ne peut être utilisé qu’en tant que DMO.

La valeur par défaut d’DMO est le mode Source. Pour sélectionner le mode de filtre, affectez à la propriété [ \_ \_ \_ \_ mode Source MFPKEY WMAAECMA DMO](mfpkey-wmaaecma-dmo-source-modeproperty.md) la valeur **Variant \_ false**.

Ensuite, configurez les propriétés internes de l’interface DMO à l’aide de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . La seule propriété qu’une application doit définir est la propriété du [ \_ \_ \_ mode système MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md) . Cette propriété configure le pipeline de traitement dans DMO. Les autres propriétés sont facultatives.

### <a name="2-set-the-input-and-output-formats"></a>2. définir les formats d’entrée et de sortie

Si vous utilisez DMO en mode filtre, définissez le format d’entrée en appelant [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). Le format d’entrée peut être quasiment n’importe quel type audio à virgule flottante PCM ou IEEE non compressé valide. Si le format d’entrée ne correspond pas au format de sortie, DMO effectue automatiquement la conversion du taux d’échantillonnage.

Si vous utilisez DMO en mode Source, ne définissez pas le format d’entrée. DMO configure automatiquement le format d’entrée en fonction des périphériques audio.

Dans l’un ou l’autre mode, définissez le format de sortie en appelant [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). DMO peut accepter les formats de sortie suivants :

-   Sous-type : **MEDIASUBTYPE \_ PCM** ou **MEDIASUBTYPE \_ IEEE \_ float**
-   Bloc de format : [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Échantillons par seconde : 8 000 ; 11 025 ; 16 000 ; ou 22 050
-   Canaux : 1 pour le mode AEC uniquement, 2 ou 4 pour le traitement du tableau de microphone
-   Bits par échantillon : 16

Le code suivant définit le type de sortie sur un audio PCM monocanal 16 bits :


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. traiter les données

Avant de traiter des données, il est recommandé d’appeler [**IMediaObject :: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Cette méthode alloue les ressources utilisées en interne par DMO. Appelez **AllocateStreamingResources** après les étapes indiquées précédemment, pas avant. Si vous n’appelez pas cette méthode, DMO alloue automatiquement les ressources lors du démarrage du traitement des données.

Si vous utilisez DMO en mode filtre, vous devez transmettre les données d’entrée à la requête DMO en appelant [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). Les données audio du microphone passent à Stream 0, et les données audio de la ligne Speaker sont transmises à Stream 1. Si vous utilisez DMO en mode Source, vous n’avez pas besoin d’appeler **ProcessInput**.

Pour récupérer les données de sortie du DSP, procédez comme suit :

1.  Créez un objet de mémoire tampon pour stocker les données de sortie. L’objet buffer doit implémenter l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . La taille de la mémoire tampon dépend des exigences de votre application. L’allocation d’une mémoire tampon plus grande peut réduire les risques de problème.
2.  Déclarez une structure de [**tampon de \_ données de sortie \_ \_ DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) et définissez le membre **pbuffer** pour qu’il pointe vers votre objet buffer.
3.  Transmettez la structure de [**\_ tampon de \_ données \_ de sortie DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) à la méthode [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) .
4.  Continuez à appeler cette méthode aussi longtemps que la méthode DMO contient des données de sortie. Le DSP signale qu’il a plus de sortie en définissant l’indicateur de **\_ données de sortie DMO \_ \_ BUFFERF \_ incomplet** dans le membre **dwStatus** de la structure de tampon de [**\_ \_ données \_ de sortie DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
