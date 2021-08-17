---
description: Les fonctions de service téléphonique supplémentaires sont répertoriées par catégorie dans les rubriques suivantes.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: fonctions de Service de Téléphone supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ee0e32260ac3821fd06e7e8962ab2a6186fb42f1140eb6cd8f705709f2dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861417"
---
# <a name="supplementary-phone-service-functions"></a>fonctions de Service de Téléphone supplémentaires

Les fonctions de service téléphonique supplémentaires sont répertoriées par catégorie dans les rubriques suivantes. Une fonction est identifiée comme [*asynchrone*](a-tapgloss.md) si elle indique la fin d’un message de réponse à l’application. Si la fonction retourne toujours son résultat à l’application immédiatement, la fonction est considérée comme [*synchrone*](s-tapgloss.md).

Voici un regroupement fonctionnel des fonctions supplémentaires de service téléphonique :

-   [Boutons](#buttons)
-   [Zones de données](#data-areas)
-   [Affichage](#display)
-   [Appareils hookswitch](#hookswitch-devices)
-   [Lampes](#lamps)
-   [Ouverture et fermeture des appareils téléphoniques](#opening-and-closing-phone-devices)
-   [initialisation et arrêt de Téléphone](#phone-initialization-and-shutdown)
-   [état et fonctionnalités de Téléphone](#phone-status-and-capabilities)
-   [négociation de version de Téléphone](#phone-version-negotiation)
-   [Anneau](#ring)
-   [État](#status)

## <a name="phone-initialization-and-shutdown"></a>Téléphone Initialisation et arrêt



| Fonction                                       | Description                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | Initialise l’abstraction de téléphone TAPI pour une utilisation par l’application appelante. Synchronous. |
| [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | Arrête l’utilisation par l’application de l’abstraction téléphonique de l’interface TAPI. Synchronous.            |



 

## <a name="phone-version-negotiation"></a>Téléphone Négociation de version



| Fonction                                                     | Description                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Permet à une application de négocier une version TAPI à utiliser. Synchronous. |



 

## <a name="opening-and-closing-phone-devices"></a>ouverture et fermeture des appareils Téléphone



| Fonction                         | Description                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | Ouvre l’appareil téléphonique spécifié, en accordant à l’application des privilèges de propriétaire ou de surveillance. Synchronous. |
| [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | Ferme un appareil téléphonique ouvert spécifié. Synchronous.                                                        |



 

## <a name="phone-status-and-capabilities"></a>Téléphone État et fonctionnalités



| Fonction                                       | Description                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | Retourne les fonctionnalités d’un appareil téléphonique donné. Synchronous.                                                                                                   |
| [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | Retourne un ID d’appareil pour la classe d’appareil donnée associée à l’appareil téléphonique spécifié. Synchronous.                                                          |
| [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | Permet à une application de récupérer une icône à afficher à l’utilisateur. Synchronous.                                                                                  |
| [**phoneConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | Fait en sorte que le fournisseur de l’appareil téléphonique spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés à l’appareil mobile. Synchronous. |



 

## <a name="hookswitch-devices"></a>Appareils hookswitch



| Fonction                                         | Description                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | Définit l’état du raccordement des appareils hookswitch d’un téléphone ouvert sur un mode spécifié. Asynchrone.      |
| [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | Interroge le mode hookswitch d’un appareil hookswitch sur un appareil téléphonique ouvert. Synchronous.          |
| [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | Définit le volume du haut-parleur d’un appareil hookswitch d’un appareil téléphonique ouvert. Asynchrone.           |
| [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | Retourne le paramètre de volume du haut-parleur d’un appareil hookswitch d’un appareil téléphonique ouvert. Synchronous. |
| [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | Définit le gain du MIC d’un appareil hookswitch d’un appareil téléphonique ouvert. Asynchrone.                 |
| [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | Retourne le paramètre de gain du MIC d’un appareil hookswitch d’un téléphone ouvert. Synchronous.              |



 

## <a name="display"></a>Affichage



| Fonction                                   | Description                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | Écrit des informations sur l’affichage d’un appareil téléphonique ouvert. Asynchrone. |
| [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | Retourne le contenu actuel de l’affichage d’un téléphone. Synchronous.          |



 

## <a name="ring"></a>Anneau



| Fonction                             | Description                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | Sonne un appareil téléphonique ouvert en fonction d’un mode de sonnerie donné. Asynchrone. |
| [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | Retourne le mode de sonnerie actuel d’un appareil téléphonique ouvert. Synchronous.    |



 

## <a name="buttons"></a>Boutons



| Fonction                                         | Description                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | Définit les informations associées à un bouton sur un appareil téléphonique. Asynchrone. |
| [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | Retourne les informations associées à un bouton sur un appareil téléphonique. Synchronous.   |



 

## <a name="lamps"></a>Lampes



| Fonction                             | Description                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | Illumine une lampe sur un appareil téléphonique ouvert spécifié dans un mode d’éclairage donné de la lampe. Asynchrone. |
| [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | Retourne le mode de lampe actuel de la lampe spécifiée. Synchronous.                           |



 

## <a name="data-areas"></a>Zones de données



| Fonction                             | Description                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | Télécharge une mémoire tampon de données dans une zone de données donnée du périphérique téléphonique. Asynchrone.      |
| [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | Charge le contenu d’une zone de données donnée dans le périphérique téléphonique dans une mémoire tampon. Synchronous. |



 

## <a name="status"></a>Statut



| Fonction                                                 | Description                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | Spécifie les modifications d’État pour lesquelles l’application souhaite être notifiée. Synchronous. |
| [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | Retourne les modifications d’État pour lesquelles l’application souhaite être notifiée. Synchronous.   |
| [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | Retourne l’état complet d’un appareil téléphonique ouvert. Synchronous.                         |



 

 

 



