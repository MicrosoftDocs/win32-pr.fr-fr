---
description: La classe CVideoTransformFilter est principalement conçue comme une classe de base pour les filtres de décompresseur AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: CVideoTransformFilter, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846814"
---
# <a name="cvideotransformfilter-class"></a>CVideoTransformFilter, classe

![hiérarchie de la classe cvideotransformfilter](images/vtsip01.png)

La `CVideoTransformFilter` classe est principalement conçue comme une classe de base pour les filtres de décompresseur avi. Cette classe ajoute la prise en charge du contrôle de qualité à la classe [**CTransformFilter**](ctransformfilter.md) . La méthode **Receive** du filtre peut décider de supprimer des frames, en fonction des messages de qualité du convertisseur et des mesures de performances collectées par le filtre pendant la diffusion en continu.

Si le filtre supprime un frame, il continue à déposer des frames jusqu’à ce qu’il atteigne l’image clé suivante. Pour les flux MPEG, le filtre ne fait pas la distinction entre les frames B et les images P.



| Variables membres protégées                                                      | Description                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | Indique si le filtre a supprimé des frames.                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | Indique si le filtre supprime actuellement des frames.                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | Durée moyenne nécessaire pour décoder une image.                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | Indique la durée pendant laquelle les exemples arrivent au convertisseur.                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | Nombre de trames reçues par le filtre depuis la dernière image clé.                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | Intervalle le plus grand observé entre les images clés.                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | Nombre maximal actuel d’images Delta à supprimer.                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | Durée nécessaire pour décoder l’exemple le plus récent.                                  |
| Méthodes protégées                                                               | Description                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Utilisé pour signaler une erreur de diffusion en continu.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifie le filtre qu’une modification de qualité est demandée.                                        |
| [**Çoive**](cvideotransformfilter-receive.md)                                | Reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Détermine si le filtre doit supprimer un échantillon spécifié.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Appelé lorsque le filtre bascule à l’état suspendu.                                           |
| M&#233;thodes publiques                                                                  | Description                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Méthode de constructeur.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Termine une opération de vidage.                                                                        |



 

 

 



