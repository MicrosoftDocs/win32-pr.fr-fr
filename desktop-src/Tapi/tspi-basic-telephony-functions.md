---
description: Tous les fournisseurs de services doivent implémenter les fonctions de téléphonie de base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Fonctions de téléphonie de base TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f5b8b4b61da6462588115463bc56b7a573e6f81215d0f9a1189983762a21062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034129"
---
# <a name="tspi-basic-telephony-functions"></a>Fonctions de téléphonie de base TSPI

Tous les fournisseurs de services doivent implémenter les fonctions de téléphonie de base. Voici une liste de ces fonctions par catégorie. Une fonction est identifiée comme *asynchrone* si elle indique la fin d’un message de réponse à l’application. Si la fonction retourne toujours son résultat immédiatement, la fonction est considérée comme *synchrone*.

-   [Adresses](#addresses)
-   [Réponse aux appels entrants](#answering-incoming-calls)
-   [Appeler des fonctions Drop](#call-drop-functions)
-   [États d’appel et événements](#call-states-and-events)
-   [État de ligne et fonctionnalités](#line-status-and-capabilities)
-   [Négociation de version de ligne](#line-version-negotiation)
-   [Appels effectués](#making-calls)
-   [Ouverture et fermeture des appareils en ligne](#opening-and-closing-line-devices)
-   [Téléphone Négociation de version](#phone-version-negotiation)
-   [Initialisation et arrêt du TSP](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>Initialisation et arrêt du TSP



|  Fonction                                                         |   Description                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Installe un TSP. Synchronous.                              |
| [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Installe le TSP. Obsolète avec la version 2,0. Synchronous. |
| [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Initialise le TSP. Synchronous.                         |
| [**TSPI \_ providerShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Arrête le fournisseur de services.                          |
| [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Supprime un TSP. Synchronous.                               |
| [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Supprime un TSP. Obsolète avec la version 2,0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Téléphone Négociation de version



|  Fonction                                                         |   Description                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Retourne la version SPI la plus élevée que le fournisseur de services peut utiliser pour cet appareil. |



 

## <a name="line-version-negotiation"></a>Négociation de version de ligne



|  Fonction                                                         |   Description                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Permet à une application de négocier une version de TSPI à utiliser avec un périphérique de ligne donné. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>État de ligne et fonctionnalités



|  Fonction                                                         |   Description                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Retourne les fonctionnalités d’un périphérique de ligne donné. Synchronous.                                                                                                  |
| [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Retourne la configuration d’un périphérique de flux multimédia. Synchronous.                                                                                                   |
| [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Retourne l’état actuel du périphérique en ligne ouvert spécifié. Synchronous.                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Définit la configuration du périphérique de flux multimédia spécifié. Synchronous.                                                                                      |
| [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Spécifie les modifications d’État pour lesquelles l’application doit être notifiée. Synchronous.                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Récupère un ID d’appareil associé à l’ouverture de ligne, à l’adresse ou à l’appel spécifié. Synchronous.                                                                  |
| [**TSPI \_ lineGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Permet à une application de récupérer une icône à afficher à l’utilisateur. Synchronous.                                                                                |
| [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Fait en sorte que le fournisseur du périphérique de ligne spécifié affiche une boîte de dialogue qui permet à l’utilisateur de configurer les paramètres liés au périphérique de ligne. Synchronous. |
| [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Affiche une boîte de dialogue qui permet à l’utilisateur de modifier les informations de configuration d’un périphérique en ligne. Synchronous.                                                    |



 

## <a name="addresses"></a>Adresses



|  Fonction                                                         |   Description                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Retourne les fonctions de téléphonie d’une adresse. Synchronous.                           |
| [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Retourne l’état actuel d’une adresse spécifiée. Synchronous.                              |
| [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Récupère le nombre d’identificateurs d’adresse pris en charge sur la ligne indiquée.             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Récupère l’ID d’adresse d’une adresse spécifiée à l’aide d’un autre format. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Ouverture et fermeture des appareils en ligne



|  Fonction                                                         |   Description                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Ouvre un appareil de ligne spécifié pour fournir une surveillance et/ou un contrôle ultérieurs de la ligne. Synchronous. |
| [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Ferme un appareil de ligne ouvert spécifié. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>États d’appel et événements



|  Fonction                                                         |   Description                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Retourne des informations fixes sur un appel. Synchronous.                                |
| [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Retourne les informations d’état de l’appel complet pour l’appel spécifié. Synchronous.       |
| [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Définit le champ propre à l’application de la structure d’informations d’un appel. Synchronous. |



 

## <a name="making-calls"></a>Appels effectués



|  Fonction                                                         |   Description                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Effectue un appel sortant et retourne un handle d’appel pour celui-ci. Asynchrone. |
| [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Compose des adresses (parties d’une ou de plusieurs) adresses à distance. Asynchrone.         |



 

## <a name="answering-incoming-calls"></a>Réponse aux appels entrants



|  Fonction                                                         |   Description                                                        |
|---------------------------------------------|-----------------------------------------|
| [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Répond à un appel entrant. Asynchrone. |



 

## <a name="call-drop-functions"></a>Appeler des fonctions Drop



|  Fonction                                                         |   Description                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Déconnecte un appel ou abandonne une tentative d’appel en cours. Asynchrone. |



 

 

 
