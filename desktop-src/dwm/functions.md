---
title: Fonctions DWM
description: Cette section contient des informations sur les fonctions de Gestionnaire de fenêtrage (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gestionnaire de fenêtrage (DWM), référence
- DWM (Gestionnaire de fenêtrage), référence
- Gestionnaire de fenêtrage (DWM), fonctions
- DWM (Gestionnaire de fenêtrage), fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd25ecbea1f7e08d8a7d5832d01908fc088e9be2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918044"
---
# <a name="dwm-functions"></a>Fonctions DWM

Cette section contient des informations sur les fonctions de Gestionnaire de fenêtrage (DWM).

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br /> | Cette fonction n’est pas implémentée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br /> | Procédure de fenêtre par défaut pour le test de positionnement DWM au sein de la zone non cliente.<br /> Vous devez également vous assurer que <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> est appelé pour le message <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> . Si <strong>DwmDefWindowProc</strong> n’est pas appelé pour le message <strong>WM_NCMOUSELEAVE</strong> , DWM ne supprime pas la mise en surbrillance des boutons <strong>agrandir</strong>, <strong>réduire</strong>et <strong>Fermer</strong> lorsque le curseur quitte la fenêtre.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br /> | Cette fonction n’est pas implémentée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br /> | Active l’effet de flou sur une fenêtre spécifiée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br /> | Active ou désactive la composition DWM. <br /><blockquote>[!Note]<br />Cette fonction est déconseillée à partir de Windows 8. DWM ne peut plus être désactivé par programmation.</blockquote><br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br /> | Notifie le DWM d’accepter ou de refuser la planification de service de planification de classe multimédia (MMCSS) pendant que le processus appelant est actif.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br /> | Étend le frame de fenêtre dans la zone cliente.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br /> | Émet un appel de vidage qui bloque l’appelant jusqu’au présent suivant, lorsque toutes les mises à jour de surface Microsoft DirectX actuellement en suspens ont été effectuées. Cela compense les scènes très complexes ou les processus appelant avec une priorité très faible.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br /> | Récupère la couleur actuelle utilisée pour la composition du verre DWM. Cette valeur est basée sur le modèle de couleurs actuel et peut être modifiée par l’utilisateur. Les applications peuvent écouter les modifications de couleur en gérant la notification de <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br /> | Récupère les informations de minutage de la composition actuelle pour une fenêtre spécifiée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br /> | Cette fonction n’est pas implémentée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br /> | Cette fonction n’est pas implémentée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br /> | Récupère les attributs de transport.<br /> | 
| <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br /> | <blockquote><strong>Remarque</strong>  cette fonction est publiquement disponible, mais non fonctionnelle, pour Windows 10, version 1803.</blockquote>Vérifie la configuration requise pour obtenir des onglets dans la barre de titre de l’application pour la fenêtre spécifiée.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br /> | Récupère la valeur actuelle d’un attribut spécifié appliqué à une fenêtre.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br /> | Appelée par une application pour indiquer que toutes les images bitmap sous forme fournies précédemment à partir d’une fenêtre, à la fois des miniatures et des représentations de lecture, doivent être actualisées.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br /> | Obtient une valeur qui indique si la composition DWM est activée. les Applications sur les ordinateurs exécutant Windows 7 ou une version antérieure peuvent écouter les changements d’état de composition en gérant la notification <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br /> | Modifie le nombre d’actualisations de l’analyse à l’aide desquelles le frame précédent s’affiche. <br /><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> n’est plus pris en charge. à partir de Windows 8.1, les appels à <strong>DwmModifyPreviousDxFrameDuration</strong> retournent toujours E_NOTIMPL.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br /> | Récupère la taille source de la miniature DWM.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br /> | Crée une relation de miniature DWM entre les fenêtres de destination et sources.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br /> | Notifie DWM qu’un contact tactile a été reconnu comme un geste et que le DWM doit dessiner des commentaires pour ce mouvement.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br /> | Définit le nombre d’actualisations de l’analyse à l’aide desquelles afficher le frame présenté. <br /><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> n’est plus pris en charge. à partir de Windows 8.1, les appels à <strong>DwmSetDxFrameDuration</strong> retournent toujours E_NOTIMPL.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br /> | Définit une image bitmap statique, sous forme pour afficher un <em>aperçu instantané</em> (également appelé <em>Aperçu avant impression</em>) d’une fenêtre ou d’un onglet. La barre des tâches peut utiliser cette image bitmap pour afficher un aperçu complet d’une fenêtre ou d’un onglet.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br /> | Définit une image bitmap statique, sous forme sur une fenêtre ou un onglet à utiliser comme représentation miniature. La barre des tâches peut utiliser cette image bitmap comme cible de commutateur de miniatures pour la fenêtre ou l’onglet.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br /> | Définit les paramètres présents pour la composition de frame. <br /><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> n’est plus pris en charge. à partir de Windows 8.1, les appels à <strong>DwmSetPresentParameters</strong> retournent toujours E_NOTIMPL.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br /> | Définit la valeur des attributs de rendu non-client pour une fenêtre.<br /> | 
| <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br /> | Appelé par une application ou une infrastructure pour spécifier le type de retour visuel à dessiner en réponse à un contact tactile ou de stylet particulier.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br /> | Active les commentaires graphiques des interactions tactiles et de glissement pour l’utilisateur.<br /> | 
| <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br /> | Coordonne les animations des fenêtres outil avec le DWM.<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br /> | Supprime une relation de miniature DWM créée par la fonction <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .<br /> | 
| <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br /> | Met à jour les propriétés d’une miniature DWM.<br /> | 




 

 

