---
title: Capture en continu à partir d’un périphérique MCI
description: Capture en continu à partir d’un périphérique MCI
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (Media Control Interface), capture en continu
- Message WM_CAP_SET_MCI_DEVICE
- capSetMCIDeviceName macro)
- Message WM_CAP_GET_MCI_DEVICE
- capGetMCIDeviceName macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d469465f47e908bda2512261ea638ad23e931a43cbb0449df676829469c3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892589"
---
# <a name="streaming-capture-from-an-mci-device"></a>Capture en continu à partir d’un périphérique MCI

Les périphériques MCI augmentent l’opération de capture en temps réel de capture et de capture de frame. Vous pouvez spécifier l’appareil MCI, tel qu’un enregistreur videodisc ou Video-cassette (VCR), agissant comme source vidéo pour votre opération de capture à l’aide du message de l' [**\_ appareil WM embout \_ Set \_ MCI \_**](wm-cap-set-mci-device.md) (ou de la macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) ) et en spécifiant le nom de l’appareil. Vous pouvez également récupérer le nom de l’appareil actuellement défini à l’aide du message [**WM \_ Cap \_ obtenir un \_ \_ appareil MCI**](wm-cap-get-mci-device.md) (ou la macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) ).

Dans la capture en temps réel, la fenêtre de capture synchronise l’opération de capture et compense les retards associés au positionnement de la source vidéo MCI et à l’initialisation des ressources (telles que les mémoires tampons de capture) requises pour la capture des données. La fenêtre de capture attend qu’un périphérique vidéo MCI valide soit installé dans le système pour capturer les données de cette manière.

Les spécifications de contrôle d’un périphérique MCI sont stockées dans les membres de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Les sources vidéo compatibles MCI incluent les magnétoscopes et les LaserDiscs. Si le membre **fMCIControl** de cette structure a la valeur **true**, la fenêtre de capture coordonne l’opération MCI. La fenêtre de capture utilise les paramètres spécifiés dans les membres **dwMCIStartTime** et **dwMCIStopTime** pour obtenir les positions de départ et d’arrêt, en millisecondes, de la séquence. Si la valeur de **fMCIControl** est **false**, la source vidéo n’est pas traitée comme un périphérique MCI et le contenu de **dwMCIStartTime** et **dwMCIStopTime** est ignoré.

Vous pouvez utiliser le lecteur multimédia pour vérifier rapidement qu’un périphérique vidéo MCI est correctement connecté au système. La lecture d’un appareil avec le lecteur multimédia vérifie que la configuration MCI pour l’appareil est correcte. Si une image apparaît sur l’affichage vidéo, la source vidéo est correctement connectée au matériel de capture.

Dans la capture d’image pas à pas, la fenêtre de capture synchronise l’opération de capture et compense les retards associés à l’emplacement de la source vidéo MCI et à l’initialisation des ressources nécessaires à la capture des données. En outre, la fenêtre de capture garantit qu’aucun frame n’est supprimé. Il parcourt les images vidéo individuellement, garantissant ainsi que le frame est capturé et stocké avant de capturer le cadre suivant dans le flux vidéo.

Les spécifications pour le contrôle de la capture d’image pas à pas sont stockées dans les membres de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . La capture d’image pas à pas utilise les membres suivants en plus des membres utilisés pour la capture en temps réel : **fStepMCIDevice**, **fStepCaptureAt2x** et **wStepCaptureAverageFrames**. Si le membre **fStepMCIDevice** a la valeur **true**, la fenêtre de capture coordonne la capture d’image pas à pas. La fenêtre de capture utilise les paramètres spécifiés dans les membres **dwMCIStartTime** et **dwMCIStopTime** pour les positions de départ et d’arrêt, en millisecondes, de la séquence. La fenêtre de capture utilise **fStepCaptureAt2x** pour déterminer si le matériel de capture doit capturer des images vidéo à deux reprises de la résolution normale et utilise **wStepCaptureAverageFrames** pour spécifier le nombre de fois où chaque trame dans l’opération de capture est échantillonnée.

Si **fStepMCIDevice** a la **valeur false**, la capture en temps réel est utilisée à la place de la capture d’image pas à pas et le contenu de **fStepCaptureAt2x**, et **wStepCaptureAverageFrames** sont ignorés.

Si une capture d’image pas à pas est spécifiée et que **fStepCaptureAt2x** est défini sur **true**, le matériel de capture capture à deux reprises la résolution spécifiée. (Les résolutions de la hauteur et de la largeur sont doublées.) Le logiciel interpole les pixels de l’image de résolution supérieure pour produire l’image à la résolution spécifiée. Cette forme de moyenne peut améliorer la définition de l’arête des images dans un cadre. Vous pouvez activer cette option si le matériel ne prend pas en charge la décimalisation basée sur le matériel et que vous capturez le format RVB.

> [!Note]  
> Si votre matériel prend en charge la décimalisation basée sur le matériel, il peut capturer des échantillons à une fréquence supérieure à celle spécifiée et utiliser ces exemples supplémentaires pour obtenir des définitions de couleurs plus cohérentes avec l’image d’origine. Les exemples supplémentaires sont ignorés une fois qu’ils sont utilisés et le matériel passe des exemples au pilote de capture à la fréquence spécifiée.

 

Si une capture d’image pas à pas est spécifiée, le membre **wStepCaptureAverageFrames** spécifie le nombre de fois où une image est échantillonnée lors de la création d’un frame basé sur l’échantillon moyen. Cette technique de calcul de la moyenne réduit le bruit de numérisation aléatoire apparaissant dans un cadre. Une valeur typique pour le nombre de moyennes est 5.

Pour plus d’informations sur MCI, consultez [MCI](mci.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Variations de capture](capture-variations.md)
</dt> </dl>

 

 




