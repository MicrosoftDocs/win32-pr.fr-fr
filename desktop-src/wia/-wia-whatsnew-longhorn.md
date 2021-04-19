---
description: De nombreuses nouvelles API WIA (Windows Image Acquisition) sont incluses dans l’acquisition d’images Windows (WIA) 2,0.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Nouveautés de l’acquisition d’images Windows (WIA) 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f9d225185b8f1ff2d6441a7ddf0e8fd919ac98
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106545212"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Nouveautés de l’acquisition d’images Windows (WIA) 2,0

De nombreuses nouvelles API WIA (Windows Image Acquisition) sont incluses dans l’acquisition d’images Windows (WIA) 2,0. En outre, il existe des incompatibilités ascendantes et descendantes entre l’acquisition d’images Windows (WIA) 1,0 et le service WIA 2,0 fourni avec Windows Vista. Certaines interfaces, structures, propriétés et valeurs de propriété de WIA 1,0 ne sont pas prises en charge par, et les applications qui les utilisent ne s’exécuteront pas sur, Windows Vista et versions ultérieures. De même, les applications qui utilisent les nouvelles interfaces, structures, propriétés et valeurs de propriété introduites avec WIA 2,0 (voir ci-dessous) ne s’exécuteront pas sur les versions de système d’exploitation antérieures à Windows Vista.

## <a name="new-api-for-wia-20"></a>Nouvelle API pour WIA 2,0

### <a name="constants-lists-updated-for-wia-20"></a>Constantes : listes mises à jour pour WIA 2,0

-   [**Constantes de propriété d’élément WIA courantes**](-wia-wiaitempropcommonitem.md)
-   [**Constantes de propriété d’informations sur l’appareil**](-wia-wiadeviceinfoprop.md)
-   [**Constantes de propriété de périphérique de scanneur**](-wia-wiaitempropscannerdevice.md)
-   [**Constantes de propriété d’élément WIA du scanneur**](-wia-wiaitempropscanneritem.md)
-   [**GUID de catégorie d’élément WIA 2,0**](-wia-wia2-itemcategoryguids.md)
-   [**Constantes de taille de page WIA 2,0**](-wia-wia2-pagesizeconstants.md)
-   [**Indicateurs de type d’élément WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Nouvelles structures dans WIA 2,0



| Rubrique                                               | Contenu                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Définit les données nécessaires pour appeler une boîte de dialogue d’appareil.<br/>                                                                                                                                                                                                       |
| [**\_ \_ en-tête brut WIA**](-wia-wia-raw-header.md)     | La structure d' [**\_ \_ en-tête brut WIA**](-wia-wia-raw-header.md) définit une image au format de données brutes d’un appareil et permet aux applications d’utiliser le format brut dans les transferts WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | Le [**WiaTransferParams**](-wia-wiatransferparams.md) est transmis à une application lors d’un transfert de données par le système d’exécution WIA à la méthode [**IWiaTransferCallback :: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Nouvelles interfaces dans WIA 2,0



| Rubrique                                                         | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Utilisé par les applications pour énumérer les objets [**IWiaItem2**](-wia-iwiaitem2.md) dans le dossier actif de l’arborescence d’éléments.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | L’interface [**IScanProfile**](-wia-iscanprofile.md) représente un profil de numérisation unique et permet aux applications de définir et d’obtenir les propriétés du profil. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | L’interface [**IScanProfileMgr**](-wia-iscanprofilemgr.md) fournit des méthodes pour créer, ouvrir, supprimer et gérer des profils d’analyse. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | L’interface [**IScanProfileUI**](-wia-iscanprofileui.md) permet aux applications d’afficher une boîte de dialogue afin que les utilisateurs puissent créer, modifier et supprimer des profils de numérisation.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | L’interface [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) permet aux applications d’afficher des fenêtres d’erreur (pendant les transferts de données) à partir desquelles l’utilisateur peut choisir de continuer, d’annuler ou d’abandonner le transfert.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | L’interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) est utilisée pour créer et gérer des appareils d’acquisition d’images et pour s’inscrire afin de recevoir des événements d’appareil.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | L’interface [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md) fournit des méthodes pour gérer les erreurs qui peuvent se produire lorsqu’une application demande des données d’image, qu’il s’agisse d’un aperçu ou de bits finaux. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | L’interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) est une interface d’extension implémentée par les développeurs de filtre de traitement d’image et appelée par WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | L’interface [**IWiaItem2**](-wia-iwiaitem2.md) fournit aux applications les mêmes fonctionnalités que l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la capacité à interroger des appareils pour découvrir leurs fonctionnalités, à accéder aux interfaces de transfert de données et aux propriétés d’élément, et à contrôler l’appareil). Il fournit également à l’application la possibilité de créer et d’utiliser dynamiquement des filtres de traitement d’images qui peuvent être des extensions des pilotes de périphériques WIA 2,0 fournis dans Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | L’interface [**IWiaPreview**](-wia-iwiapreview.md) met en cache les images non filtrées en interne et les transmet via des filtres de traitement d’image. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | L’interface [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) détecte les sous-régions d’un flux d’image et crée des éléments [**IWiaItem2**](-wia-iwiaitem2.md) distincts pour chacun. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | L’interface [**IWiaTransfer**](-wia-iwiatransfer.md) fournit un transfert de données basé sur les flux. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | L’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) reçoit des rappels pendant un transfert de données. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | L’interface IWiaUIExtension2 fournit des méthodes qui remplacent la valeur par défaut, l’interface utilisateur fournie par le système par une interface utilisateur personnalisée, et qui fournissent une icône d’appareil personnalisée. Les fournisseurs d’appareils peuvent implémenter cette interface pour fournir des interfaces utilisateur personnalisées pour leurs appareils.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Présentations nouvelles et modifiées pour WIA 2,0



| Rubrique                                                                          | Contenu |
|--------------------------------------------------------------------------------|----------|
| [Constantes](-wia-constants.md)                                                |          |
| [Fonctions](-wia-functions.md)                                                |          |
| [Interfaces](-wia-interfaces.md)                                              |          |
| [Analyser le schéma de profil](-wia-scan-profile-schema.md)                            |          |
| [Structures](-wia-structures.md)                                              |          |
| [Transfert de données d’image dans WIA 2,0](-wia-transferring-image-data-in-wia2.md) |          |
| [Spécificateurs de type d’appareil WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Constantes de propriété WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Conserver les commentaires

Messagerie électronique **sdkfdbk@microsoft.com** pour envoyer des rapports d’erreurs et des demandes de fonctionnalités directement à Microsoft.

 

 




