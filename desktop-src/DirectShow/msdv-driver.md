---
description: Pilote MSDV
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: Pilote MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5377471f61944c60f57720df6bc64482681d64515f54c853d78cfa405842ff15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748617"
---
# <a name="msdv-driver"></a>Pilote MSDV

MSDV est le pilote WDM (Microsoft Windows Driver Model) pour les caméscopes DV. le pilote apparaît comme un filtre de DirectShow lorsque l’appareil est branché. Elle est énumérée dans deux catégories de filtre :

-   CLSID \_ VideoInputDeviceCategory ("Video capture sources")
-   AM \_ KSCATEGORY \_ Render (« périphériques de rendu de streaming WDM »)

Le nom convivial du filtre est `Microsoft DV Camera and VCR` , ou un équivalent localisé. Dans certains appareils, la propriété **Description** contient une description du modèle spécifique, qui peut être utilisée à la place du nom convivial générique. Pour plus d’informations, consultez [sélection d’un périphérique de capture](selecting-a-capture-device.md).

MSDV a deux broches de sortie. Un code confidentiel fournit des images DV qui contiennent des données audio et vidéo entrelacées. L’autre code PIN fournit des images vidéo uniquement sans audio. MSDV ne peut pas diffuser en continu à partir des deux broches en même temps, de sorte qu’une seule broche de sortie peut être connectée à la fois. Pour plus d’informations sur la capture de vidéos à partir d’un périphérique DV, consultez la section [capture DV dans un fichier](capture-dv-to-file.md).

![capture de données DV à partir de l’appareil](images/dv-filters4.png)

La plupart des caméscopes DV disposent d’une sous-unité d’enregistreur vidéo (magnétoscope), qui peut transmettre des données de la bande à l’ordinateur. Pour l’application, la capture à partir d’une bande fonctionne de la même façon que la capture vidéo en direct. La seule différence est que l’application doit contrôler le transport de bande externe : Démarrer et arrêter la bande, rembobiner, etc. À cet effet, MSDV expose les interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)et [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) . Pour plus d’informations sur le contrôle d’un magnétoscope, consultez [contrôle d’un caméscope DV](controlling-a-dv-camcorder.md).

Vous pouvez également transmettre le DV de l’ordinateur au caméscope. La vidéo peut ensuite être affichée sur l’écran intégré du caméscope ou enregistrée sur bande. Pour prendre en charge cette fonctionnalité, MSDV a une broche d’entrée qui peut recevoir un flux DV entrelacé. Lorsque la broche d’entrée est connectée, MSDV agit comme un filtre de convertisseur à la place d’un filtre de capture. MSDV ne prend pas en charge la recherche dans ce mode. Pour plus d’informations sur l’envoi de données DV à l’appareil, consultez [transmettre le fichier DV du fichier à la bande](transmit-dv-from-file-to-tape.md).

![transmission de données DV à l’appareil](images/dv-filters5.png)

Notez que les broches d’entrée et de sortie ne peuvent pas être connectées en même temps, car l’appareil ne peut pas diffuser les deux sens en même temps.

Dans de nombreux caméscopes, le basculement entre le mode VTR et le mode caméra provoque la désactivation de l’appareil. par conséquent, DirectShow risque de perdre l’appareil quand l’utilisateur change de mode. Pour plus d’informations sur les événements de suppression d’appareils, consultez [notification de suppression d’appareil](device-removal-notification.md).

## <a name="remarks"></a>Remarques

Pour plus d’informations sur les formats DV pris en charge par le pilote MSDV, consultez la page relative aux [**sous-types vidéo DV**](dv-video-subtypes.md).

Quelques conseils sur la création de graphiques de filtre avec MSDV :

-   Vous ne pouvez pas utiliser [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) pour restituer une broche de sortie sur MSDV. (le gestionnaire de Graph de filtre tente de connecter la broche de sortie à la broche d’entrée de MSDV, qui échoue.) utilisez plutôt [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ou [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).
-   Lorsqu’un graphique de filtre contient MSDV, MSDV doit fournir l’horloge de référence pour le graphique. à partir de DirectX 8,0, le gestionnaire de Graph de filtre choisit automatiquement MSDV comme horloge de référence. avec les versions antérieures, vous devez appeler la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) sur le gestionnaire de Graph de filtre. Pour plus d’informations sur les horloges, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).
-   en fonction de l’appareil, certaines méthodes de **IAMExtDevice**, **IAMExtTransport** et **IAMTimeCodeReader** peuvent retourner Windows codes d’erreur au lieu de valeurs **HRESULT** . Les codes d’erreur possibles sont les suivants :

    | Code d'erreur              | Description                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | \_délai d’erreur          | Une commande d’appareil externe a dépassé le délai d’attente.                                                        |
    | ERREUR \_ req \_ non \_ ACCEP  | L’appareil n’a pas accepté cette commande de périphérique externe.                                          |
    | ERREUR \_ non \_ prise en charge   | L’appareil ne prend pas en charge cette commande d’appareil externe.                                        |
    | demande d’erreur \_ \_ abandonnée | Une commande d’appareil externe a été abandonnée. L’appareil a peut-être été supprimé ou la réinitialisation du bus s’est produite. |

    

     

### <a name="device-information"></a>Informations sur l'appareil

dans Windows Millennium Edition et Windows XP, le moniker de l’appareil du filtre DV prend en charge une propriété **Description** en plus de la propriété **FriendlyName** . Cette propriété renvoie une description de l’appareil, extraite du fichier INF, qui contient généralement le nom de la personnalisation de l’appareil. Toutefois, cette propriété n’est pas prise en charge pour tous les modèles d’appareil.

Pour plus d’informations sur les monikers de périphérique, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).

### <a name="clock-times"></a>Heures d’horloge

Le pilote MSDV utilise l’horloge 1394 Bus contenue dans les paquets de données 1394 pour dériver l’horloge. Il utilise ces valeurs pour horodater les exemples de média DV. Étant donné que cette horloge source n’est pas l’horloge système de l’ordinateur, les heures finissent par se dépasser de l’horloge système de l’ordinateur. comme indiqué ci-dessus, toutefois, par défaut, le gestionnaire de Graph de filtre sélectionne MSDV comme horloge de référence du graphique.

L’interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) signale la mesure actuelle du pilote des frames supprimés. Cette valeur peut ne pas être parfaitement synchronisée avec le nombre réel d’images supprimées à un moment donné. Si des frames sont supprimés, cela indique que le système n’est pas équilibré (la production des données dépasse la consommation des données). Par exemple, le disque dur de l’utilisateur peut ne pas être suffisamment rapide pour prendre en charge les taux de capture DV.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



