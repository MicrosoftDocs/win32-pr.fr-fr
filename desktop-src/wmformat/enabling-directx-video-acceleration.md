---
title: Activation de l’accélération vidéo DirectX
description: Activation de l’accélération vidéo DirectX
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- Windows Media Format SDK, activation de DXVA
- Windows Media Format SDK, DirectX Video Acceleration (DXVA)
- Windows Media Format SDK, accélération vidéo
- ASF (Advanced Systems Format), activation d’DXVA
- ASF (format avancé des systèmes), activer DXVA
- Advanced Systems Format (ASF), DirectX Video Acceleration (DXVA)
- ASF (format des systèmes avancés), accélération vidéo DirectX (DXVA)
- ASF (Advanced Systems Format), accélération vidéo
- ASF (format des systèmes avancés), accélération vidéo
- DirectX Video Acceleration (DXVA), activation
- DXVA (DirectX Video Acceleration), activation
- Accélération vidéo DirectX (DXVA), ordre des opérations
- DXVA (DirectX Video Acceleration), ordre des opérations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381481"
---
# <a name="enabling-directx-video-acceleration"></a>Activation de l’accélération vidéo DirectX

Cette section décrit comment activer l’accélération vidéo de Microsoft® DirectX® lors de la lecture de contenu diffusé en continu dans un lecteur personnalisé.

## <a name="background"></a>Arrière-plan

DirectX Video Acceleration (DirectX VA) est une spécification d’API pour l’accélération matérielle des opérations de décodage 2D. Il permet aux décodeurs logiciels de décharger certaines opérations gourmandes en ressources du processeur vers la carte graphique en vue de leur traitement. Pour les utilisateurs finaux, cela rend possible une vidéo à débit élevé, telle que la lecture de DVD plein écran sur des ordinateurs plus anciens équipés de cartes graphiques compatibles DirectX VA.

À partir du kit de développement logiciel (SDK) Windows Media Format 9 Series, le filtre de wrappers DMO prend en charge DirectX VA. Cela signifie que, pour la lecture locale, les applications peuvent utiliser le filtre de lecteur ASF WM pour lire le contenu Windows Media et l’accélération matérielle DirectX VA sera appelée automatiquement si la carte graphique le prend en charge. Toutefois, le filtre de lecteur ASF WM ne prend pas en charge la lecture de contenu diffusé en continu. Par conséquent, si vous souhaitez prendre en charge DirectX VA lors de la lecture de contenu diffusé dans un lecteur personnalisé, vous devez utiliser un autre mécanisme, qui est celui utilisé par le lecteur Windows Media à partir de la série Windows Media 9.

Étant donné que le lecteur Windows Media a été conçu avant le développement des filtres QASF, le lecteur Windows Media dispose de son propre filtre source, basé sur le kit de développement logiciel (SDK) Windows Media format, pour la lecture de contenu Windows Media. Le filtre de source Windows Media WMP fournit des données décompressées en aval directement aux convertisseurs audio et vidéo. En revanche, le lecteur ASF WM fournit du contenu compressé en aval du décodeur Windows Media DMOs (DirectX Media Objects), qui sont hébergés dans le wrapper DMO. Les diagrammes suivants illustrent les différences entre le lecteur ASF WM et le filtre de source Windows Media WMP.

![le filtre source personnalisé génère des exemples non compressés](images/wmp-dxva-graph.png)

![exemples de sorties de filtre source qasf compressés](images/qasf-dxva-graph.png)

Pour activer DirectX VA pour le contenu diffusé en continu, vous devez créer un filtre source personnalisé comme celui du diagramme supérieur. En fait, ce filtre utilise le kit de développement logiciel (SDK) Windows Media format pour instancier un objet WM Reader, décompresser les exemples et les envoyer en aval sur ses broches de sortie. Cette discussion part du principe que vous avez déjà créé le filtre source et que vous êtes maintenant prêt à implémenter la prise en charge DirectX VA.

Pour activer DirectX VA, la tâche de base du filtre source consiste à fournir au convertisseur vidéo et au décodeur WMV DMO les interfaces dont il a besoin pour négocier la connexion DirectX VA. Le filtre source ne participe pas à ces négociations. Après le démarrage de la diffusion en continu, la seule tâche du filtre source que le filtre source peut effectuer est de modifier les horodatages sur les échantillons vidéo avant que le décodeur WMV les remette au convertisseur vidéo. La raison principale pour cela est de fournir un contrôle de chronologie personnalisé au-delà de ce que les interfaces de® DirectShow standard activent.

Trois interfaces sont définies pour activer les communications nécessaires entre le kit de développement logiciel (SDK) du format Windows Media, le filtre source du lecteur, le Windows Media Video décoder DMO, le mélangeur de superposition ou le convertisseur de mixage vidéo. Ces interfaces sont décrites dans le tableau suivant.



| Interface                                                        | Description                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Exposée par le décodeur Windows Media DMO et appelée par le filtre source d’un lecteur multimédia pour configurer les différentes connexions requises pour activer DirectX VA afin de décoder le contenu de Windows Media Video. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Implémenté sur le filtre source du lecteur. Il permet au filtre de modifier les horodatages sur les échantillons vidéo avant de les diffuser en aval.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Implémenté sur l’objet WM Reader. Elle est appelée par un filtre de source de lecteur pour obtenir des interfaces à partir du décodeur DMO.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Ordre des opérations dans DirectX VA-lecture activée

Cette section décrit l’ordre général des opérations au moment de l’exécution pour un lecteur prenant en charge DirectX VA et son filtre source. Les composants référencés dans cette section sont les suivants :

-   Un lecteur multimédia tiers, appelé lecteur.
-   Filtre source personnalisé, instancié par le lecteur, qui utilise le kit de développement logiciel (SDK) Windows Media format pour décompresser le contenu multimédia Windows.
-   Broche de sortie vidéo du filtre source du joueur, appelée broche de sortie.
-   Le graphique de filtre de lecture vidéo DirectShow, désigné sous le terme de graphique.
-   Convertisseur de mixage vidéo, appelé VMR.
-   Objet lecteur asynchrone du kit de développement logiciel (SDK) Windows Media format, appelé lecteur.
-   Objet média DirectX du décodeur Windows Media Video, appelé décodeur DMO.

L’ordre des opérations est le suivant :

1.  Le lecteur instancie son filtre source et un objet lecteur. Le lecteur crée un décodeur vidéo DMO et définit le type d’entrée (compressé) sur celui-ci. Cela doit se produire avant que le lecteur ne tente de configurer son graphique de lecture vidéo car le kit de développement logiciel (SDK) et le décodeur DMO doivent être impliqués dans le processus de négociation avec le graphique, et le modèle d’entrée doit connaître le format d’entrée à l’étape 9.
2.  Le lecteur appelle **IGraphBuilder :: Render**, en lui fournissant la broche de sortie du filtre de la source vidéo. À ce stade, le gestionnaire de graphe de filtre DirectShow tente de connecter VMR au filtre de source vidéo du lecteur.
3.  Le gestionnaire de graphique de filtre appelle **IPIN :: Connect** sur la broche de sortie du filtre de source vidéo du lecteur.

Les étapes 4 à 10 se produisent à l’intérieur de **IPIN :: Connect**.

1.  Le filtre source obtient l’interface **IWMCodecAMVideoAccelerator** à partir de la méthode **IWMReaderAccelerator :: GetCodecInterface** du lecteur. Si le codec ne prend pas en charge DirectX VA, l’appel à **GetCodecInterface** peut échouer. Dans ce cas, la négociation se poursuit normalement, sans prise en charge de DirectX VA.
2.  Le filtre source passe le pointeur **IAMVideoAccelerator** à partir du code confidentiel transmis à la **connexion** au décodeur DMO via **IWMCodecAMVideoAccelerator :: SetAcceleratorInterface**.
3.  Le filtre source délègue ensuite le reste de l’opération **IPIN :: Connect** à la méthode **CBaseOutputPin :: Connect** . L’énumération de format avec le kit de développement logiciel (SDK) s’exécute aujourd’hui. Si le codec prend en charge DirectX VA pour le contenu en cours de connexion, le codec DMO présente les sous-types DirectX VA en premier, avant les types YUV et RGB pris en charge. Si la prise en charge de DirectX VA est disponible, les étapes 7 à 11 sont tentées dans le contexte d’un sous-type DirectX VA. L’extrait de code suivant montre comment identifier un sous-type de média DirectX VA.
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  L’implémentation de **CBaseOutputPin :: Connect** appelle **IPIN :: CompleteConnect** à l’étape 3. Si un sous-type DirectX VA est pris en compte, la négociation DirectX VA est tentée. La broche de sortie appelle **IWMCodecAMVideoAccelerator :: NegotiateConnection**, en lui transmettant le type de média de sortie actuel.
5.  Le décodeur DMO effectue la négociation requise avec VMR via l’interface **IAMVideoAccelerator** et retourne le GUID de sous-type de vidéo que les deux ont convenu. La broche de sortie délègue tous les appels **IAMVideoAcceleratorNotify** reçus au cours de ce processus à l’interface **IAMVideoAcceleratorNotify** du décodeur DMO, qui peut également être obtenue par le biais de la méthode **IWMReaderAccelerator :: GetCodecInterface** .
6.  Si **NegotiateConnection** fonctionne, la broche de sortie appelle **IWMCodecAMVideoAccelerator :: SetPlayerNotify** avec une interface **IWMPlayerTimestampHook** . Ce hook permet au filtre source de mettre à jour les horodatages sur les échantillons avant qu’ils ne soient transmis au convertisseur.
7.  Le filtre source appelle **IWMReaderAccelerator :: Notify** avec le type de média négocié. Cela permet au lecteur de mettre à jour ses variables internes et de la valider sur DirectX VA. Il s’agit du dernier emplacement où le codec ou le lecteur peut échouer. Si l’une des étapes ci-dessus échoue, le filtre source doit revenir à l’étape 3 et essayer le type suivant énuméré par le lecteur.
8.  La lecture démarre. Le lecteur ignore les mémoires tampons de sortie du décodeur DMO si le type de sortie de la connexion est DirectX VA.
9.  Quand **IPIN ::D éconnecter** se produit, le filtre source appelle **IWMCodecAMVideoAccelerator :: SetAcceleratorInterface** avec une **valeur null**. Cela rompt la connexion DirectX VA entre le codec et le convertisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




